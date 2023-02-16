Some Random notes and reverse engineering and testing various UUIDv3/5 by kydavis@cisco.com

### DNS UUID Namespace
`6ba7b810-9dad-11d1-80b4-00c04fd430c8`

### DNS UUID Namespace No Dashes
`6ba7b8109dad11d180b400c04fd430c8`

### DNS UUID Namespace as Integer
`143098242404177361603877621312831893704`

### Example Name
`www.example.com`

### Expected v3 MD5 UUID
`5df41881-3aed-3515-88a7-2f4a814cf09e`

### v5 SHA1 UUID
`2ed6657d-e927-568b-95e1-2665a8aea6a2`

---

### Python Byte Conversions
```python
>>> (143098242404177361603877621312831893704).to_bytes(16, byteorder='big')
b'k\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0O\xd40\xc8'

>>> bytes("www.example.com", "utf-8")
b'www.example.com'
```

### MD5 in Bash, missing dashes, needs var and ver bits set.
Note Python groups a few together more than 2 hex chars but grouping ever two has the same result
```bash
kydavis@ubuntu-server:~$ echo -n -e "k\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0O\xd40\xc8www.example.com" | md5sum
5df418813aed051548a72f4a814cf09e  -
```

### SHA1 in Bash, missing dashes, needs var and ver bits set.
```bash
kydavis@ubuntu-server:~$ echo -n -e "k\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0O\xd40\xc8www.example.com" | sha1sum
2ed6657de927468b55e12665a8aea6a22dee3e35  -
```

----------------------------

# Putting all the steps together in Bash
Misc bash commands: `echo`, `sed`, `bc`, `awk`, `md5sum`, `sha1sum`, `sha256sum`

Purely for understanding the individual steps in greater detail, not super practical

### MD5 - 5df41881-3aed-3515-88a7-2f4a814cf09e
```bash
# Unset vars
unset namespace
unset name
unset namespaceIDoctetString
unset hash
unset variantSpace
unset variant
unset newvVariant

# Set Vars
namespace=6ba7b810-9dad-11d1-80b4-00c04fd430c8
name=www.example.com

# Convert Namespace into string of octets
# \x6b\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0\x4f\xd4\x30\xc8
namespaceIDoctetString=$(echo -n $namespace | sed 's/-//g' | sed 's/.\{2\}/\\x&/g')

# Compute hash
# 5df418813aed051548a72f4a814cf09e
hash=$(echo -n -e $namespaceIDoctetString$name | md5sum)

# Get the variant hex, convert to uppercase for BC in next step
# 4
variantSpace=$(echo $hash | sed -r 's/^.{16}(.{1}).{15}.*/\1/' | tr '[:lower:]' '[:upper:]')

# Convert hex to bin ensure always 4 char length and replace upper two chars with 1 and 0
# 1000
variant=$(echo "obase=2; ibase=16; $variantSpace" | bc | awk '{ printf "%04d\n", $0 }' | sed -r 's/.*(..)$/10\1/')

# convert back to hex
# 8
newVariant=$(echo "obase=16; ibase=2; $variant" | bc)

# replace Ver (3) and Var, add Dashes, anything remaining is dropped, convert back to lowercase
echo $hash | sed -r 's/^(.{12}).{1}(.{19})/\13\2/' | sed -re "s/(.{8})(.{4}).{1}(.{3}).{1}(.{3})(.{12}).*/\1-\2-3\3-$newVariant\4-\5/" | tr '[:upper:]' '[:lower:]'
# 5df41881-3aed-3515-88a7-2f4a814cf09e
```

### SHA1 - 2ed6657d-e927-568b-95e1-2665a8aea6a2
```bash
# Unset vars
unset namespace
unset name
unset namespaceIDoctetString
unset hash
unset variantSpace
unset variant
unset newvVariant

# Set Vars
namespace=6ba7b810-9dad-11d1-80b4-00c04fd430c8
name=www.example.com

# Convert Namespace into string of octets
# \x6b\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0\x4f\xd4\x30\xc8
namespaceIDoctetString=$(echo -n $namespace | sed 's/-//g' | sed 's/.\{2\}/\\x&/g')

# Compute hash
# 2ed6657de927468b55e12665a8aea6a22dee3e35
hash=$(echo -n -e $namespaceIDoctetString$name | sha1sum)

# Get the variant hex, convert to uppercase for BC in next step
# 5
variantSpace=$(echo $hash | sed -r 's/^.{16}(.{1}).{15}.*/\1/' | tr '[:lower:]' '[:upper:]')

# Convert hex to bin ensure always 4 char length and replace upper two chars with 1 and 0
# 1001
variant=$(echo "obase=2; ibase=16; $variantSpace" | bc | awk '{ printf "%04d\n", $0 }' | sed -r 's/.*(..)$/10\1/')

# convert back to hex
# 9
newVariant=$(echo "obase=16; ibase=2; $variant" | bc)

# replace Ver (5) and Var, add Dashes, anything remaining is dropped, convert back to lowercase
echo $hash | sed -r 's/^(.{12}).{1}(.{19})/\13\2/' | sed -re "s/(.{8})(.{4}).{1}(.{3}).{1}(.{3})(.{12}).*/\1-\2-5\3-$newVariant\4-\5/" | tr '[:upper:]' '[:lower:]'
# 2ed6657d-e927-568b-95e1-2665a8aea6a2
```

### SHA256 (Testing a "v8) - 401835fd-a627-870a-873f-ed73f2bc5b2c
```bash
# Unset vars
unset hashspace
unset namespace
unset name
unset namespaceIDoctetString
unset hash
unset variantSpace
unset variant
unset newvVariant

# Set Vars
hashspace=3fb32780-953c-4464-9cfd-e85dbbe9843d
namespace=6ba7b810-9dad-11d1-80b4-00c04fd430c8
name=www.example.com

# Convert Hashspace into string of octets
# \x3f\xb3\x27\x80\x95\x3c\x44\x64\x9c\xfd\xe8\x5d\xbb\xe9\x84\x3d
hashspaceIDoctetString=$(echo -n $hashspace | sed 's/-//g' | sed 's/.\{2\}/\\x&/g')

# Convert Namespace into string of octets
# \x6b\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0\x4f\xd4\x30\xc8
namespaceIDoctetString=$(echo -n $namespace | sed 's/-//g' | sed 's/.\{2\}/\\x&/g')

# Compute hash
# 401835fda627a70a073fed73f2bc5b2c2a8936385a38a9c133de0ca4af0dfaed
hash=$(echo -n -e $hashspaceIDoctetString$namespaceIDoctetString$name | sha256sum)

# Get the variant hex, convert to uppercase for BC in next step
# 0
variantSpace=$(echo $hash | sed -r 's/^.{16}(.{1}).{15}.*/\1/' | tr '[:lower:]' '[:upper:]')

# Convert hex to bin ensure always 4 char length and replace upper two chars with 1 and 0
# 1000
variant=$(echo "obase=2; ibase=16; $variantSpace" | bc | awk '{ printf "%04d\n", $0 }' | sed -r 's/.*(..)$/10\1/')

# convert back to hex
# 8
newVariant=$(echo "obase=16; ibase=2; $variant" | bc)

# replace Ver (8) and Var, add Dashes, anything remaining is dropped, convert back to lowercase
echo $hash | sed -r 's/^(.{12}).{1}(.{19})/\13\2/' | sed -re "s/(.{8})(.{4}).{1}(.{3}).{1}(.{3})(.{12}).*/\1-\2-8\3-$newVariant\4-\5/" | tr '[:upper:]' '[:lower:]'
# 401835fd-a627-870a-873f-ed73f2bc5b2c
```

```python
import hashlib
import uuid

# predefined by RFC 4122
NAMESPACE_DNS = uuid.UUID("6ba7b810-9dad-11d1-80b4-00c04fd430c8")

# predefined by new RFC (UUIDv4s I just made up for example)
ALGORITHM_SHA256 = uuid.UUID("3fb32780-953c-4464-9cfd-e85dbbe9843d")

# concatenate hash_algorithm_uuid + namespace_uuid + name; then hash
sha256 = hashlib.new("sha256")
sha256.update(ALGORITHM_SHA256.bytes)
sha256.update(NAMESPACE_DNS.bytes)
sha256.update(bytes("www.example.com", "utf-8"))
print(sha256.hexdigest())
```

---

### SHA256 (Testing a "v9") - 5c146b14-3c52-9afd-938a-375d0df1fbf6
```bash
# Unset vars
unset namespace
unset name
unset namespaceIDoctetString
unset hash
unset variantSpace
unset variant
unset newvVariant

# Set Vars
namespace=6ba7b810-9dad-11d1-80b4-00c04fd430c8
name=www.example.com

# Convert Namespace into string of octets
# \x6b\xa7\xb8\x10\x9d\xad\x11\xd1\x80\xb4\x00\xc0\x4f\xd4\x30\xc8
namespaceIDoctetString=$(echo -n $namespace | sed 's/-//g' | sed 's/.\{2\}/\\x&/g')

# Compute hash
# 5c146b143c524afd938a375d0df1fbf6fe12a66b645f72f6158759387e51f3c8
hash=$(echo -n -e $namespaceIDoctetString$name | sha256sum)

# Get the variant hex, convert to uppercase for BC in next step
# 9
variantSpace=$(echo $hash | sed -r 's/^.{16}(.{1}).{15}.*/\1/' | tr '[:lower:]' '[:upper:]')

# Convert hex to bin ensure always 4 char length and replace upper two chars with 1 and 0
# 1001
variant=$(echo "obase=2; ibase=16; $variantSpace" | bc | awk '{ printf "%04d\n", $0 }' | sed -r 's/.*(..)$/10\1/')

# convert back to hex
# 9
newVariant=$(echo "obase=16; ibase=2; $variant" | bc)

# replace Ver (9) and Var, add Dashes, anything remaining is dropped, convert back to lowercase
echo $hash | sed -r 's/^(.{12}).{1}(.{19})/\13\2/' | sed -re "s/(.{8})(.{4}).{1}(.{3}).{1}(.{3})(.{12}).*/\1-\2-9\3-$newVariant\4-\5/" | tr '[:upper:]' '[:lower:]'
# 5c146b14-3c52-9afd-938a-375d0df1fbf6
```

---

# Testing and Comparing Results

### Python3 
- https://github.com/python/cpython/blob/main/Lib/uuid.py
```python
>>> import uuid
>>> uuid.uuid3(uuid.NAMESPACE_DNS, "www.example.com")
UUID('5df41881-3aed-3515-88a7-2f4a814cf09e')
>>> uuid.uuid5(uuid.NAMESPACE_DNS, "www.example.com")
UUID('2ed6657d-e927-568b-95e1-2665a8aea6a2')
>>>
```

### UUID Tools (PHP) 
- https://github.com/aarreedd/uuidtools.com
- https://www.uuidtools.com/api/generate/v3/namespace/6ba7b810-9dad-11d1-80b4-00c04fd430c8/name/base64:d3d3LmV4YW1wbGUuY29t
- https://www.uuidtools.com/api/generate/v5/namespace/6ba7b810-9dad-11d1-80b4-00c04fd430c8/name/base64:d3d3LmV4YW1wbGUuY29t

### Javascript - https://github.com/uuidjs/uuid/blob/main/src/v35.js
TODO

### uuidgen (libuud) 
- https://github.com/util-linux/util-linux/blob/master/misc-utils/uuidgen.c
- https://github.com/util-linux/util-linux/blob/master/libuuid/src/gen_uuid.c
```c
kydavis@ubuntu-server:~$ uuidgen -m -N www.example.com -n @dns
5df41881-3aed-3515-88a7-2f4a814cf09e

kydavis@ubuntu-server:~$ uuidgen -s -N www.example.com -n @dns
2ed6657d-e927-568b-95e1-2665a8aea6a2
```

---

# Other Notes
- uuidgen with an MD5 hash where variant was hex xb computes the new var to x9, all others compute to xb as b1011 already has first two bits set to 10 and modifying them is null.
- Seems uuidgen (actually libuuid) are doing little endian or misunderstood which bits to change because of errata https://www.rfc-editor.org/errata/eid4976
- Inputs of DNS namespace and www.kyzer.me as the name confirm allow an MD5 hash with var as xb before modification
```
kydavis@ubuntu-server:~$ uuidgen -m -N www.kyzer.me -n @dns
df6b5e88-8e20-3136-9785-e44f079d0b78

>>> import uuid
>>> uuid.uuid3(uuid.NAMESPACE_DNS, "www.kyzer.me")
UUID('df6b5e88-8e20-3136-b785-e44f079d0b78')
```
