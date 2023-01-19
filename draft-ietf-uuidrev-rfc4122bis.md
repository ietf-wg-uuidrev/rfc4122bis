---
v: 3
docname: draft-ietf-uuidrev-rfc4122bis-latest
cat: std
obsoletes: '4122'
consensus: 'true'
submissiontype: IETF
pi:
  strict: 'yes'
  toc: 'yes'
  tocdepth: '3'
  symrefs: 'yes'
  sortrefs: 'yes' # accidentally correcting accident :-)
title: A Universally Unique IDentifier (UUID) URN Namespace
abbrev: A UUID URN Namespace
area: ART
wg: uuidrev
kw: uuid
date: 2022

author:
- ins: P. Leach
  name: P. Leach
  email: paulle@microsoft.com
  org: Microsoft
- ins: M. Mealling
  name: M. Mealling
  email: michael@refactored-networks.com
  org: VeriSign, Inc.
- name: Brad G. Peabody
  email: brad@peabody.io
- name: Kyzer R. Davis
  email: kydavis@cisco.com
  org: Cisco Systems

normative:
  NCA:
    title: Network Computing Architecture
    author:
    - ins: L. Zahn
      name: L. Zahn
      org: ''
    - ins: T. Dineen
      name: T. Dineen
      org: ''
    - ins: P. Leach
      name: P. Leach
      org: ''
    date: 1990-01
    seriesinfo:
      ISBN: 0-13-611674-4
  C309:
    target: https://pubs.opengroup.org/onlinepubs/9696999099/toc.pdf
    title: "DCE: Remote Procedure Call"
    rc: Open Group CAE Specification C309
    seriesinfo:
      ISBN: 1-85912-041-5
    date: August 1994
  X667:
    seriesinfo:
      ISO/IEC: '9834-8:2004'
      ITU-T Rec.: X.667
    title: >
      Information Technology, "Procedures for the
      operation of OSI Registration Authorities: Generation and
      registration of Universally Unique Identifiers (UUIDs) and their
      use as ASN.1 Object Identifier components"
    date: 2004
  RFC1321: RFC1321
  RFC6151: RFC6151
  RFC4086: RFC4086
  RFC8141: RFC8141
  RFC4234: RFC4234
  RFC6194: RFC6194
  SHA1:
    target: https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf
    title: Secure Hash Standard
    author:
    - org: National Institute of Standards and Technology
    date: August 2015
    seriesinfo:
      FIPS: PUB 180-4
  C311:
    target: https://pubs.opengroup.org/onlinepubs/9696989899/toc.pdf
    title: "DCE 1.1: Authentication and Security Services"
    rc: Open Group CAE Specification C311
    date: 1997
informative:
  LexicalUUID:
    target: https://github.com/twitter-archive/cassie
    title: A Scala client for Cassandra
    author:
    - org: Twitter
    date: 2012-11
    seriesinfo:
      commit: f6da4e0
  Snowflake:
    target: https://github.com/twitter-archive/snowflake/releases/tag/snowflake-2010
    title: >
      Snowflake is a network service for generating unique ID numbers at high
      scale with some simple guarantees.
    author:
    - org: Twitter
    date: 2014-05
    seriesinfo:
      Commit: b3f6a3c
  Flake:
    target: https://github.com/boundary/flake
    title: 'Flake: A decentralized, k-ordered id generation service in Erlang'
    author:
    - org: Boundary
    date: 2017-02
    seriesinfo:
      Commit: 15c933a
  ShardingID:
    target: https://instagram-engineering.com/sharding-ids-at-instagram-1cf5a71e5a5c
    title: Sharding & IDs at Instagram
    author:
    - org: Instagram Engineering
    date: 2012-12
  KSUID:
    target: https://github.com/segmentio/ksuid
    title: K-Sortable Globally Unique IDs
    author:
    - org: Segment
    date: 2020-07
    seriesinfo:
      Commit: bf376a7
  Elasticflake:
    target: https://github.com/ppearcy/elasticflake
    title: Sequential UUID / Flake ID generator pulled out of elasticsearch common
    author:
    - name: Paul Pearcy
    date: 2015-01
    seriesinfo:
      Commit: dd71c21
  FlakeID:
    target: https://github.com/T-PWK/flake-idgen
    title: Flake ID Generator
    author:
    - name: Tom Pawlak
    date: 2020-04
    seriesinfo:
      Commit: fcd6a2f
  Sonyflake:
    target: https://github.com/sony/sonyflake
    title: A distributed unique ID generator inspired by Twitter's Snowflake
    author:
    - org: Sony
    date: 2020-08
    seriesinfo:
      Commit: 848d664
  orderedUuid:
    target: https://itnext.io/laravel-the-mysterious-ordered-uuid-29e7500b4f8
    title: 'Laravel: The mysterious "Ordered UUID"'
    author:
    - name: Italo Baeza Cabrera
    date: 2020-01
  COMBGUID:
    target: https://github.com/richardtallent/RT.Comb
    title: Creating sequential GUIDs in C# for MSSQL or PostgreSql
    author:
    - name: Richard Tallent
    date: 2020-12
    seriesinfo:
      Commit: '2759820'
  ULID:
    target: https://github.com/ulid/spec
    title: Universally Unique Lexicographically Sortable Identifier
    author:
    - name: Alizain Feerasta
    date: 2019-05
    seriesinfo:
      Commit: d0c7170
  SID:
    target: https://github.com/chilts/sid
    title: 'sid : generate sortable identifiers'
    author:
    - name: Andrew Chilton
    date: 2019-06
    seriesinfo:
      Commit: 660e947
  pushID:
    target: https://firebase.googleblog.com/2015/02/the-2120-ways-to-ensure-unique_68.html
    title: The 2^120 Ways to Ensure Unique Identifiers
    author:
    - org: Google
    date: 2015-02
  XID:
    target: https://github.com/rs/xid
    title: Globally Unique ID Generator
    author:
    - name: Olivier Poitrey
    date: 2020-10
    seriesinfo:
      Commit: efa678f
  ObjectID:
    target: https://docs.mongodb.com/manual/reference/method/ObjectId/
    title: ObjectId - MongoDB Manual
    author:
    - org: MongoDB
    date: false # XXX check
  CUID:
    target: https://github.com/ericelliott/cuid
    title: Collision-resistant ids optimized for horizontal scaling and performance.
    author:
    - name: Eric Elliott
    date: 2020-10
    seriesinfo:
      Commit: 215b27b
  IEEE754:
    target: https://standards.ieee.org/ieee/754/6210/
    title: IEEE Standard for Floating-Point Arithmetic.
    author:
    - org: IEEE
    date: 2019-07
    seriesinfo:
      Series: 754-2019
  URNNamespaces:
    target: https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml
    title: Uniform Resource Names (URN) Namespaces
    author:
    - org: IANA
    date: 2022-11-18

--- abstract

This specification defines a Uniform Resource Name namespace for
UUIDs (Universally Unique IDentifier), also known as GUIDs (Globally
Unique IDentifier).  A UUID is 128 bits long, and can guarantee
uniqueness across space and time.  UUIDs were originally used in the
Apollo Network Computing System and later in the Open Software
Foundation's (OSF) Distributed Computing Environment (DCE), and then
in Microsoft Windows platforms.

This specification is derived from the DCE specification with the
kind permission of the OSF (now known as The Open Group).
Information from earlier versions of the DCE specification have been
incorporated into this document.

--- middle

# Introduction {#Background}

This specification defines a Uniform Resource Name namespace for
UUIDs (Universally Unique IDentifier), also known as GUIDs (Globally
Unique IDentifier).  A UUID is 128 bits long, and requires no central
registration process.

The information here is meant to be a concise guide for those wishing
to implement services using UUIDs as URNs {{RFC8141}}.  Nothing in this document
should be construed to override the DCE standards that defined UUIDs.

There is an ITU-T Recommendation and ISO/IEC Standard {{X667}} that are
derived from earlier versions of this document.  Both sets of
specifications have been aligned, and are fully technically
compatible.  In addition, a global registration function is being
provided by the Telecommunications Standardization Bureau of ITU-T;
for details see [](https://www.itu.int/en/ITU-T/asn1/Pages/UUID/uuids.aspx).

# Motivation {#motivation}

One of the main reasons for using UUIDs is that no centralized
authority is required to administer them (although one format uses
IEEE 802 node identifiers, others do not).  As a result, generation
on demand can be completely automated, and used for a variety of
purposes.  The UUID generation algorithm described here supports very
high allocation rates of up to 10 million per second per machine if
necessary, so that they could even be used as transaction IDs.

UUIDs are of a fixed size (128 bits) which is reasonably small
compared to other alternatives.  This lends itself well to sorting,
ordering, and hashing of all sorts, storing in databases, simple
allocation, and ease of programming in general.

Since UUIDs are unique and persistent, they make excellent Uniform
Resource Names.  The unique ability to generate a new UUID without a
registration process allows for UUIDs to be one of the URNs with the
lowest minting cost.

Furthermore, many things have changed in the time since UUIDs were originally created.
Modern applications have a need to create and utilize UUIDs as the primary
identifier for a variety of different items in complex computational systems,
including but not limited to database keys, file names, machine or system
names, and identifiers for event-driven transactions.

One area UUIDs have gained popularity is as database keys.
This stems from the increasingly distributed nature of modern applications.
In such cases, "auto increment" schemes often used by databases do not work
well, as the effort required to coordinate unique numeric identifiers across
a network can easily become a burden.
The fact that UUIDs can be used to create unique, reasonably short values
in distributed systems without requiring synchronization makes them a good
alternative, but UUID versions 1-5 lack certain other desirable characteristics:


1. Non-time-ordered UUID versions such as UUIDv4 have poor database index
  locality.
  Meaning new values created in succession are not close to each other in
  the index and thus require inserts to be performed at random
  locations.
  The negative performance effects of which on common structures used for
  this (B-tree and its variants) can be dramatic.

1. The 100-nanosecond, Gregorian epoch used in UUIDv1 timestamps is uncommon
  and difficult to represent accurately using a standard number format such
  as {{IEEE754}}.



1. Introspection/parsing is required to order by time sequence; as opposed to
  being able to perform a simple byte-by-byte comparison.



1. Privacy and network security issues arise from using a MAC address in the
  node field of Version 1 UUIDs.
  Exposed MAC addresses can be used as an attack surface to locate machines
  and reveal various other
  information about such machines (minimally manufacturer, potentially other
  details). Additionally, with the advent of virtual machines and containers,
  MAC address uniqueness is no longer guaranteed.



1. Many of the implementation details specified in RFC4122 involved trade
  offs that are neither possible to specify for all applications nor
  necessary to produce interoperable implementations.



1.  RFC4122 did not distinguish between the requirements for generation
  of a UUID versus an application which simply stores one, which are often
  different.



Due to the aforementioned issue, many widely distributed database applications
and large application vendors have sought to solve the problem of creating
a better
time-based, sortable unique identifier for use as a database key. This has
lead to numerous implementations
over the past 10+ years solving the same problem in slightly different ways.

While preparing this specification the following 16 different implementations
were analyzed for trends in total ID length, bit Layout, lexical formatting/encoding,
timestamp type, timestamp format, timestamp accuracy, node format/components,
collision handling and multi-timestamp tick generation sequencing.


{: spacing="compact"}
1. {{ULID}} by A. Feerasta
1. {{LexicalUUID}} by Twitter
1. {{Snowflake}} by Twitter
1. {{Flake}} by Boundary
1. {{ShardingID}} by Instagram
1. {{KSUID}} by Segment
1. {{Elasticflake}} by P. Pearcy
1. {{FlakeID}} by T. Pawlak
1. {{Sonyflake}} by Sony
1. {{orderedUuid}} by IT. Cabrera
1. {{COMBGUID}} by R. Tallent
1. {{SID}} by A. Chilton
1. {{pushID}} by Google
1. {{XID}} by O. Poitrey
1. {{ObjectID}} by MongoDB
1. {{CUID}} by E. Elliott

An inspection of these implementations and the issues described above has
led to this document which attempts to adapt UUIDs to address these issues.

# Terminology {#terminology}

## Requirements Language {#requirements_language}

{::boilerplate bcp14-tagged}

## Abbreviations {#acronyms}

The following abbreviations are used in this document:

{: indent="14"}
UUID
: Universally Unique Identifier

URN
: Uniform Resource Names

ABNF
: Augmented Backus-Naur Form

CSPRNG
: Cryptographically Secure Pseudo-Random Number Generator

MAC
: Media Access Control

MSB
: Most Significant Bit

DBMS
: Database Management System

IEEE
: Institute of Electrical and Electronics Engineers, Inc.

ITU
: International Telecommunication Union

MD5
: Message Digest 5

SHA1
: Secure Hash Algorithm 1

UTC
: Coordinated Universal Time



## changelog {#changelog}
{:removeinrfc}

draft-00

{: spacing="compact"}
- Merge RFC4122 with draft-peabody-dispatch-new-uuid-format-04.md
- Change: Reference RFC1321 to RFC6151
- Change: Reference RFC2141 to RFC8141
- Change: Reference RFC2234 to RFC4234
- Change: Reference FIPS 180-1 to FIPS 180-4 for SHA1
- Change: Converted UUIDv1 to match UUIDv6 section from Draft 04
- Change: Trimmed down the ABNF representation
- Change: http websites to https equivalent
- Errata: Bad Reference to RFC1750 \| 3641 #4
- Errata: Change MD5 website to example.com \| 3476 #6 (Also Fixes Errata: Fix uuid_create_md5_from_name() \| 1352 #2)
- Errata: Typo in code comment \| 6665 #11
- Errata: Fix BAD OID acronym \| 6225 #9
- Errata: Incorrect Parenthesis usage Section 4.3 \| 184 #5
- Errata: Lexicographically Sorting Paragraph Fix \| 1428 #3
- Errata: Fix 4.1.3 reference to the correct bits \| 1957 #13
- Errata: Fix reference to variant in octet 8 \| 4975 #7
- Errata: Further clarify 3rd/last bit of Variant for spec \| 5560 #8
- Errata: Fix clock_seq_hi_and_reserved most-significant bit verbiage \| 4976 #10
- Errata: Better Clarify network byte order when referencing most significant bits \| 3546 #12
- Draft 05: B.2. Example of a UUIDv7 Value two "var" in table #120
- Draft 05: MUST veribage in Reliability of 6.1 #121
- Draft 05: Further discourage centralized registry for distributed UUID Generation.
- New: Further Clarity of exact octet and bit of var/ver in this spec
- New: Block diagram, bit layout, test vectors for UUIDv4
- New: Block diagram, bit layout, test vectors for UUIDv3
- New: Block diagram, bit layout, test vectors for UUIDv5
- New: Add MD5 Security Considerations reference, RFC6151
- New: Add SHA1 Security Considerations reference, RFC6194

# UUID Format {#format}

The UUID format is 16 octets (128 bits); the variant bits in conjunction with the version
bits described in the next sections in determine finer structure.

UUIDs MAY be represented as binary data or integers.
When in use with URNs or applications, any given 128 bit UUID SHOULD
be represented by the "hex-and-dash" string format consisting of multiple
groups of upper or lowercase alphanumeric hex characters separated by a single dash/hyphen.
When used with databases please refer to {{database_considerations}}.

The formal definition of the UUID string representation is provided by the following (ABNF) {{RFC4234}}.

~~~~ abnf
   UUID                   = 4hexOctet "-"
                            2hexOctet "-"
                            2hexOctet "-"
                            2hexOctet "-"
                            6hexOctet
   hexOctet               = hexDigit hexDigit
   hexDigit =
         "0" / "1" / "2" / "3" / "4" / "5" / "6" / "7" / "8" / "9" /
         "a" / "b" / "c" / "d" / "e" / "f" /
         "A" / "B" / "C" / "D" / "E" / "F"
~~~~

An example UUID using this textual representation from the previous table observed in {{sampleHexUUID}}.
Note that in this example the alphabetic characters may be all uppercase, all lowercase or mixe case as per {{RFC4234, Section 2.3}}

~~~~
f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleHexUUID title='Example Hex UUID'}

The same UUID from {{sampleHexUUID}} is represented in Binary {{sampleBinaryUUID}}, Integer {{sampleIntegerUUID}} and as a URN {{sampleURNUUID}} defined by {{RFC8141}}.

~~~~
11111000000111010100111110101110011111011110110000010001110100001010011101100101000000001010000011001001000111100110101111110110
~~~~
{: #sampleBinaryUUID title='Example Hex UUID'}

~~~~
329800735698586629295641978511506172918
~~~~
{: #sampleIntegerUUID title='Example Hex UUID'}

~~~~
urn:uuid:f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleURNUUID title='Example Hex UUID'}

## Variant Field {#variant_field}

The variant field determines the layout of the UUID.  That is, the
interpretation of all other bits in the UUID depends on the setting
of the bits in the variant field.  As such, it could more accurately
be called a type field; we retain the original term for
compatibility.  The variant field consists of a variable number of
the most significant bits of octet 8 of the UUID.

{{table1}} lists the contents of the variant field, where
the letter "x" indicates a "don't-care" value.

| Msb0 | Msb1 | Msb2 | Description                                            |
|    0 |    x | x    | Reserved, NCS backward compatibility.                  |
|    1 |    0 | x    | The variant specified in this document.                |
|    1 |    1 | 0    | Reserved, Microsoft Corporation backward compatibility |
|    1 |    1 | 1    | Reserved for future definition.                        |
{: #table1 title='UUID Variants'}

Interoperability, in any form, with variants other than the one
defined here is not guaranteed, and is not likely to be an issue in
practice.

Specifically for UUIDs in this document bits 64 and 65 of octet 8 MUST be set to 1 and 0 as per row 2 of {{table1}}.
As such all bit and field layouts will detail a 2 bit variant entry as guidance.

## Version Field {#version_field}
The version number is in the most significant 4 bits of octet 6.
More specifically bits 48 through 51. The remaining 4 bits of Octet 6 are dynamic.

{{table2}} lists all of the versions for this UUID variant specified in this document.

| Msb0 | Msb1 | Msb2 | Msb3 | Version | Description                                                                   |
|    0 |    0 |    0 |    0 |       0 | Unused                                                                        |
|    0 |    0 |    0 |    1 |       1 | The Gregorian time-based UUID from in this document.                          |
|    0 |    0 |    1 |    0 |       2 | Reserved for DCE Security version, with embedded POSIX UUIDs.                 |
|    0 |    0 |    1 |    1 |       3 | The name-based version specified in this document that uses MD5 hashing.      |
|    0 |    1 |    0 |    0 |       4 | The randomly or pseudo-randomly generated version specified in this document. |
|    0 |    1 |    0 |    1 |       5 | The name-based version specified in this document that uses SHA-1 hashing.    |
|    0 |    1 |    1 |    0 |       6 | Reordered Gregorian time-based UUID specified in this document.               |
|    0 |    1 |    1 |    1 |       7 | Unix Epoch time-based UUID specified in this document.                        |
|    1 |    0 |    0 |    0 |       8 | Reserved for custom UUID formats specified in this document.                  |
|    1 |    0 |    0 |    1 |       9 | Reserved for future definition.                                               |
|    1 |    0 |    1 |    0 |      10 | Reserved for future definition.                                               |
|    1 |    0 |    1 |    1 |      11 | Reserved for future definition.                                               |
|    1 |    1 |    0 |    0 |      12 | Reserved for future definition.                                               |
|    1 |    1 |    0 |    1 |      13 | Reserved for future definition.                                               |
|    1 |    1 |    1 |    0 |      14 | Reserved for future definition.                                               |
|    1 |    1 |    1 |    1 |      15 | Reserved for future definition.                                               |
{: #table2 title='UUID variant 10xx (8/9/A/B) versions defined by this specification'}

An example version/variant layout for UUIDv4 follows the table
where M represents the version placement for the hex representation of 4 (0100)
and the N represents the variant placement for one of the four possible hex representation of variant 10x:
8 (1000), 9 (1001), A (1010), B (1011)

~~~~
00000000-0000-4000-8000-000000000000
00000000-0000-4000-9000-000000000000
00000000-0000-4000-A000-000000000000
00000000-0000-4000-B000-000000000000
xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
~~~~
{: title='UUIDv4 Variant Examples'}

# UUID Layouts {#layout}

To minimize confusion about bit assignments within octets and among differing versions,
the UUID record definition is defined only in terms of fields that are
integral numbers of octets.  The fields are presented with the most
significant one first.

In the absence of explicit application or presentation protocol
specification to the contrary, each field is encoded with the Most
Significant Byte first (known as network byte order).

Note that in some instances the field names, particularly for multiplexed fields, follow historical
practice.

While discussing UUID field layouts, bit definitions start at 0 and end at 127 while octets definitions start at 0 and end at 15.

## UUID Version 1 {#uuidv1}
UUID Version 1 is a time-based UUID featuring a 60-bit timestamp
represented by Coordinated Universal Time (UTC) as a count of 100-
nanosecond intervals since 00:00:00.00, 15 October 1582 (the date of
Gregorian reform to the Christian calendar).

UUID Version 1 also features clock sequence field which is used to help avoid
duplicates that could arise when the clock is set backwards in time
or if the node ID changes.

Finally the node field consists of an IEEE 802 MAC
address, usually the host address.  For systems with multiple IEEE
802 addresses, any available one can be used.  The lowest addressed
octet (octet number 10) contains the global/local bit and the
unicast/multicast bit, and is the first octet of the address
transmitted on an 802.3 LAN.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                          time_low                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|       time_mid                |         time_hi_and_version   |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|clk_seq_hi_res |  clk_seq_low  |         node (0-1)            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                         node (2-5)                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv1 Field and Bit Layout'}

{: vspace='0'}

time_low:
: The least significant 32 bits of the 60 bit starting timestamp.
  Occupies bits 0 through 31 (octets 0-3)

time_mid:
: The middle 16 bits of the 60 bit starting timestamp.
  Occupies bits 32 through 47 (octets 4-5)

time_hi_and_version:
: The first four most significant bits MUST contain
  the UUIDv1 version (0001) while the remaining 12 bits will contain
  the most significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 48 through 63 (octets 6-7)

clock_seq_hi_and_res:
: The first two bits MUST be set to the UUID variant (10)
  The remaining 6 bits contain the high portion of the clock sequence.
  Occupies bits 64 through 71 (octet 8) for a full 8 bits.

clock_seq_low:
: The 8 bit low portion of the clock sequence.
  Occupies bits 72 through 79 (octet 9)

node:
: 48 bit spatially unique identifier
  Occupies bits 80 through 127 (octets 10-15)

For systems that do not have UTC available, but do have the local
time, they may use that instead of UTC, as long as they do so
consistently throughout the system.  However, this is not recommended
since generating the UTC from local time only needs a time zone
offset.

If the clock is set backwards, or might have been set backwards
(e.g., while the system was powered off), and the UUID generator can
not be sure that no UUIDs were generated with timestamps larger than
the value to which the clock was set, then the clock sequence has to
be changed.  If the previous value of the clock sequence is known, it
can just be incremented; otherwise it should be set to a random or
high-quality pseudo-random value.

Similarly, if the node ID changes (e.g., because a network card has
been moved between machines), setting the clock sequence to a random
number minimizes the probability of a duplicate due to slight
differences in the clock settings of the machines.  If the value of
clock sequence associated with the changed node ID were known, then
the clock sequence could just be incremented, but that is unlikely.

The clock sequence MUST be originally (i.e., once in the lifetime of
a system) initialized to a random number to minimize the correlation
across systems.  This provides maximum protection against node
identifiers that may move or switch from system to system rapidly.
The initial value MUST NOT be correlated to the node identifier.

For systems with no IEEE address, a randomly or pseudo-randomly
generated value may be used; see {{unguessability}} and {{unidentifiable}}.

## UUID Version 2 {#uuidv2}
UUID Version 2 is known as DCE Security UUIDs {{C309}} and {{C311}}.
As such the definition of these UUIDs are outside the scope of this specification.

## UUID Version 3 {#uuidv3}
UUID Version 3 is meant for generating UUIDs from "names"
that are drawn from, and unique within, some "name space" as per {{name_based_uuid_generation}}.

UUIDv3 values are created by computing an MD5 {{RFC1321}}
hash over a given name space value concatenated with the desired name value
after both have been converted to a canonical sequence of octets in network byte order.
This MD5 value is then uses to populate all 128 bits of the UUID layout.
The UUID version and variant then replace the respective bits as defined by {{version_field}} and {{variant_field}}.

Some common name space values have been defined via {{namespaces}}.

Where possible UUIDv5 SHOULD be used in lieu of UUIDv3.
For more information on MD5 security considerations see {{RFC6151}}.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            md5_high                           |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          md5_high             |  ver  |       md5_mid         |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                        md5_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            md5_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv3 Field and Bit Layout'}

{: vspace='0'}

md5_high:
: The first 48 bits of the layout are filled
  with the most significant, left-most 48 bits
  from the computed MD5 value.

ver:
: The 4 bit version field as defined by {{version_field}}

md5_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following md5_high
  from the computed MD5 value.

var:
: The 2 bit variant field as defined by {{variant_field}}.

md5_low:
: The final 62 bits of the layout immediately following the var field to be
  filled with the least-significant, right-most bits of the final 64 bits
  from the computed MD5 value.

## UUID Version 4 {#uuidv4}
The version 4 UUID is meant for generating UUIDs from truly-random or
pseudo-random numbers.

An implementation may generate 128 bits of random random data which is
used to fill out the UUID fields in {{uuidv4fields}}. The UUID version
and variant then replace the respective bits as defined by {{version_field}}
and {{variant_field}},

Alternatively, an implementation MAY choose to randomly generate the exact required number of bits for
for random_a, random_b, and random_c then concatenate the version and variant in the required position.

For guidelines on random data generation see {{unguessability}}.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           random_a                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          random_a             |  ver  |       random_b        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                       random_c                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           random_c                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: id='uuidv4fields' title='UUIDv4 Field and Bit Layout'}

{: vspace='0'}

random_a:
: The first 48 bits of the layout that can be filled with random data as per {{unguessability}}
  fit.

ver:
: The 4 bit version field as defined by {{version_field}}

random_b:
: 12 more bits of the layout that can be filled random data as per {{unguessability}}

var:
: The 2 bit variant field as defined by {{variant_field}}.

random_c:
: The final 62 bits of the layout immediately following the var field to be
  filled with random data as per {{unguessability}}

## UUID Version 5 {#uuidv5}
UUID Version 5 is meant for generating UUIDs from "names"
that are drawn from, and unique within, some "name space" as per {{name_based_uuid_generation}}.

UUIDv5 values are created by computing an SHA1 {{SHA1}}
hash over a given name space value concatenated with the desired name value
after both have been converted to a canonical sequence of octets in network byte order.
This SHA1 value is then uses to populate all 128 bits of the UUID layout. Excess bits beyond 128 are discarded.
The UUID version and variant then replace the respective bits as defined by {{version_field}} and {{variant_field}}

Some common name space values have been defined via {{namespaces}}.

For more information on MD5 security considerations see {{RFC6194}}.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            sha_high                           |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          sha_high             |  ver  |       sha_mid         |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                        sha_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            md5_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv5 Field and Bit Layout'}

{: vspace='0'}

sha_high:
: The first 48 bits of the layout are filled
  with the most significant, left-most 48 bits
  from the computed SHA1 value.

ver:
: The 4 bit version field as defined by {{version_field}}

sha_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following md5_high
  from the computed SHA1 value.

var:
: The 2 bit variant field as defined by {{variant_field}}.

sha_low:
: The final 62 bits of the layout immediately following the var field to be
  filled by skipping the 2 most significant, left-most bits of the remaining SHA1 hash
  and then using the next 62 most significant, left-most bits.
  Any leftover SHA1 bits are discarded and unused.

## UUID Version 6 {#uuidv6}

UUID version 6 is a field-compatible version of UUIDv1, reordered for improved
DB locality.
It is expected that UUIDv6 will primarily be used in contexts where there
are existing v1 UUIDs.
Systems that do not involve legacy UUIDv1 SHOULD consider using UUIDv7 instead.

Instead of splitting the timestamp into the low, mid and high sections from
UUIDv1, UUIDv6 changes this sequence so timestamp bytes are stored from most
to least significant.
That is, given a 60 bit timestamp value as specified for UUIDv1 in {{uuidv1}},
for UUIDv6, the first 48 most significant bits are stored
first, followed by the 4 bit version (same position), followed by the remaining
12 bits of the original 60 bit timestamp.

The clock sequence bits remain unchanged from their usage and position in {{uuidv1}}.

The 48 bit node SHOULD be set to a pseudo-random value however implementations
MAY choose to retain the old MAC address behavior from {{uuidv1}} and {{unidentifiable}}. For more information on MAC address usage within UUIDs see the {{Security}}

The format for the 16-byte, 128 bit UUIDv6 is shown in {{v6layout}}


~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           time_high                           |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|           time_mid            |      time_low_and_version     |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|clk_seq_hi_res |  clk_seq_low  |         node (0-1)            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                         node (2-5)                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: id='v6layout' title='UUIDv6 Field and Bit Layout'}

{: vspace='0'}

time_high:
: The most significant 32 bits of the 60 bit starting timestamp.
  Occupies bits 0 through 31 (octets 0-3)

time_mid:
: The middle 16 bits of the 60 bit starting timestamp.
  Occupies bits 32 through 47 (octets 4-5)

time_low_and_version:
: The first four most significant bits MUST contain
  the UUIDv6 version (0110) while the remaining 12 bits will contain
  the least significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 48 through 63 (octets 6-7)

clk_seq_hi_res:
: The first two bits MUST be set to the UUID variant (10)
  The remaining 6 bits contain the high portion of the clock sequence.
  Occupies bits 64 through 71 (octet 8) for a full 8 bits.

clock_seq_low:
: The 8 bit low portion of the clock sequence.
  Occupies bits 72 through 79 (octet 9)

node:
: 48 bit spatially unique identifier
  Occupies bits 80 through 127 (octets 10-15)

With UUIDv6 the steps for splitting the timestamp into time_high and time_mid
are OPTIONAL
since the 48 bits of time_high and time_mid will remain in the same order.
An extra step of splitting the first 48 bits of the timestamp into the most
significant
32 bits and least significant 16 bits proves useful when reusing an existing
UUIDv1 implementation.


## UUID Version 7 {#v7}

UUID version 7 features a time-ordered value field derived from the widely
implemented and well known Unix Epoch timestamp source, the number of milliseconds
seconds since midnight 1 Jan 1970 UTC, leap seconds excluded.
As well as improved entropy characteristics over versions 1 or 6.

Implementations SHOULD utilize UUID version 7 over UUID version 1 and 6 if
possible.


~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           unix_ts_ms                          |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          unix_ts_ms           |  ver  |       rand_a          |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                        rand_b                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                            rand_b                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv7 Field and Bit Layout'}

{: vspace='0'}

unix_ts_ms:
: 48 bit big-endian unsigned number of Unix epoch timestamp as per {{timestamp_granularity}}.

ver:
: 4 bit UUIDv7 version set as per {{version_field}}

rand_a:
: 12 bits pseudo-random data to provide uniqueness as per {{monotonicity_counters}} and {{unguessability}}.

var:
: The 2 bit variant defined by {{variant_field}}.

rand_b:
: The final 62 bits of pseudo-random data to provide uniqueness as per {{monotonicity_counters}} and {{unguessability}}.


## UUID Version 8 {#v8}

UUID version 8 provides an RFC-compatible format for experimental or vendor-specific
use cases.
The only requirement is that the variant and version bits MUST be set as
defined in {{variant_field}} and {{version_field}}.
UUIDv8's uniqueness will be implementation-specific and SHOULD NOT be assumed.

The only explicitly defined bits are the Version and Variant leaving 122
bits
for implementation specific time-based UUIDs. To be clear:
UUIDv8 is not a replacement for UUIDv4 where all 122 extra bits are
filled with random data.

Some example situations in which UUIDv8 usage could occur:


* An implementation would like to embed extra information
  within the UUID other than what is defined in this document.



* An implementation has other application/language restrictions which
  inhibit the use of one of the current UUIDs.


~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           custom_a                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|          custom_a             |  ver  |       custom_b        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                       custom_c                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           custom_c                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv8 Field and Bit Layout'}

{: vspace='0'}

custom_a:
: The first 48 bits of the layout that can be filled as an implementation sees
  fit.

ver:
: The 4 bit version field as defined by {{version_field}}

custom_b:
: 12 more bits of the layout that can be filled as an implementation sees fit.

var:
: The 2 bit variant field as defined by {{variant_field}}.

custom_c:
: The final 62 bits of the layout immediately following the var field to be
  filled as an implementation sees fit.

## Nil UUID {#niluuid}
The nil UUID is special form of UUID that is specified to have all
128 bits set to zero.

~~~~
00000000-0000-0000-0000-000000000000
~~~~
{: title='Nil UUID Format'}

## Max UUID {#maxuuid}

The Max UUID is special form of UUID that is specified to have all 128 bits
set to 1. This UUID can be thought of as the inverse of Nil UUID defined
in {{niluuid}}.


~~~~
FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF
~~~~
{: title='Max UUID Format'}



# UUID Best Practices {#uuid_best_practices}

The minimum requirements for generating UUIDs are
described in this document for each version.
Everything else is an implementation detail and
up to the implementer to decide what is appropriate for a given
implementation. That being said, various relevant factors are covered
below to help guide an implementer through the different trade-offs among
differing UUID implementations.

## Timestamp Granularity {#timestamp_granularity}

UUID timestamp source, precision and length was the topic of great debate
while creating UUIDv7 for this specification. As such choosing the right timestamp for
your application is a very important topic. This section will detail some
of the most common points on this topic.

{: vspace='0'}

Reliability:
: Implementations SHOULD use the current timestamp from a reliable source to
  provide values that are time-ordered and continually increasing.
  Care SHOULD be taken to ensure that timestamp changes from the environment
  or operating system are handled in a way that is consistent with implementation
  requirements.
  For example, if it is possible for the system clock to move backward due
  to either manual adjustment or corrections from a time synchronization protocol,
  implementations need to determine how to handle such cases. (See Altering, Fuzzing,
  or Smearing bullet below.)

Source:
: UUID version 1 and 6 both utilize a Gregorian epoch timestamp while UUIDv7
  utilizes a Unix Epoch timestamp. If other timestamp sources or a custom timestamp
  epoch are required UUIDv8 SHOULD be leveraged.

Sub-second Precision and Accuracy:
: Many levels of precision exist for timestamps: milliseconds, microseconds,
  nanoseconds, and beyond.
  Additionally fractional representations of sub-second precision may be desired
  to mix various levels of precision in a time-ordered manner.
  Furthermore, system clocks themselves have an underlying granularity and
  it is frequently less than the precision offered by the operating system.
  With UUID version 1 and 6, 100-nanoseconds of precision are present while
  UUIDv7 features fixed millisecond level of precision within the Unix epoch
  that does not exceed the granularity capable in most modern systems.
  For other levels of precision UUIDv8 SHOULD be utilized.
  Similar to {{monotonicity_counters}}, with UUIDv1 or UUIDv6,
  a high resolution timestamp can be simulated by keeping a count of
  the number of UUIDs that have been generated with the same value of
  the system time, and using it to construct the low order bits of the
  timestamp.  The count will range between zero and the number of
  100-nanosecond intervals per system time interval.

Length:
: The length of a given timestamp directly impacts how long a given UUID will
  be valid.
  That is, how many timestamp ticks can be contained in a UUID before the maximum
  value for the timestamp field is reached.
  Care should be given to ensure that the proper length is selected for a given
  timestamp.
  UUID version 1 and 6 utilize a 60 bit timestamp and UUIDv7 features a 48
  bit timestamp.

Altering, Fuzzing, or Smearing:
: Implementations MAY alter the actual timestamp. Some examples included security
  considerations around providing a real clock value within a UUID, to correct
  inaccurate clocks or to handle leap seconds. This specification makes no
  requirement or guarantee about how close the clock value needs to be to actual
  time.
  If UUIDs do not need to be frequently generated, the UUIDv1 or UUIDv6 timestamp can
  simply be the system time multiplied by the number of 100-nanosecond
  intervals per system time interval.

Padding:
: When timestamp padding is required, implementations MUST pad the most significant
  bits (left-most) bits with zeros. An example is padding the most significant,
  left-most bits of a 32 bit Unix timestamp with zero's to fill out the 48
  bit timestamp in UUIDv7.

Truncating:
: Similarly, when timestamps need to be truncated: the lower, least significant
  bits MUST be used. An example would be truncating a 64 bit Unix timestamp
  to the least significant, right-most 48 bits for UUIDv7.

Error Handling:
: If a system overruns the generator by requesting too many UUIDs
  within a single system time interval, the UUID service MUST either
  return an error, or stall the UUID generator until the system clock
  catches up.
  Note that if the processors overrun the UUID generation frequently,
  additional node identifiers can be allocated to the system, which
  will permit higher speed allocation by making multiple UUIDs
  potentially available for each time stamp value.
  Similar to {{distributed_shared_knowledge}} techniques

## Monotonicity and Counters {#monotonicity_counters}

Monotonicity is the backbone of time-based sortable UUIDs. Naturally time-based
UUIDs from this document will be monotonic due to an embedded timestamp however
implementations can guarantee additional monotonicity via the concepts covered
in this section.

Additionally, care SHOULD be taken to ensure UUIDs generated in batches are
also monotonic. That is, if one-thousand UUIDs are generated for the same
timestamp; there is sufficient logic for organizing the creation order of
those one-thousand UUIDs.
For batch UUID creation implementations MAY utilize a monotonic counter which
SHOULD increment for each UUID created during a given timestamp.

For single-node UUID implementations that do not need to create batches of
UUIDs, the embedded timestamp within UUID version 1, 6, and 7 can provide
sufficient monotonicity guarantees by simply ensuring that timestamp increments
before creating a new UUID. For the topic of Distributed Nodes please refer
to {{distributed_shared_knowledge}}

Implementations SHOULD choose one method for single-node UUID implementations
that require batch UUID creation.

{: vspace='0'}

Fixed-Length Dedicated Counter Bits (Method 1):
: This references the practice of allocating a specific number of bits in the
  UUID layout to the sole purpose of tallying the total number of UUIDs created
  during a given UUID timestamp tick.
  Positioning of a fixed bit-length counter SHOULD be immediately after the
  embedded timestamp. This promotes sortability and allows random data generation
  for each counter increment.
  With this method rand_a section of UUIDv7 SHOULD be utilized as fixed-length
  dedicated counter bits that are incremented by one for every UUID generation.
  The trailing random bits generated for each new UUID in rand_b can help produce
  unguessable UUIDs. In the event more counter bits are required the most significant,
  left-most, bits of rand_b MAY be leveraged as additional counter bits.

Monotonic Random (Method 2):
: With this method the random data is extended to also double as a counter.
  This monotonic random can be thought of as a "randomly seeded counter" which
  MUST be incremented in the least significant position for each UUID created
  on a given timestamp tick.
  UUIDv7's rand_b section SHOULD be utilized with this method to handle batch
  UUID generation during a single timestamp tick.
  The increment value for every UUID generation SHOULD be a random integer
  of any desired length larger than zero. It ensures the UUIDs retain the required
  level of unguessability characters provided by the underlying entropy.
  The increment value MAY be one when the amount of UUIDs generated in a particular
  period of time is important and guessability is not an issue. However, it
  SHOULD NOT be used by implementations that favor unguessiblity, as the resulting
  values are easily guessable.

The following sub-topics cover topics related solely with creating reliable
fixed-length dedicated counters:

{: vspace='0'}

Fixed-Length Dedicated Counter Seeding:
: Implementations utilizing fixed-length counter method SHOULD randomly initialize
  the counter with each new timestamp tick.
  However, when the timestamp has not incremented; the counter SHOULD be frozen
  and incremented via the desired increment logic.
  When utilizing a randomly seeded counter alongside Method 1; the random MAY
  be regenerated with each counter increment without impacting sortability.
  The downside is that Method 1 is prone to overflows if a counter of adequate
  length is not selected or the random data generated leaves little room for
  the required number of increments.
  Implementations utilizing fixed-length counter method MAY also choose to
  randomly initialize a portion counter rather than the entire counter. For
  example, a 24 bit counter could have the 23 bits in least-significant, right-most,
  position randomly initialized. The remaining most significant, left-most
  counter bits are initialized as zero for the sole purpose of guarding against
  counter rollovers.

Fixed-Length Dedicated Counter Length:
: Care MUST be taken to select a counter bit-length that can properly handle
  the level of timestamp precision in use.
  For example, millisecond precision SHOULD require a larger counter than a
  timestamp with nanosecond precision.
  General guidance is that the counter SHOULD be at least 12 bits but no longer
  than 42 bits.
  Care SHOULD also be given to ensure that the counter length selected leaves
  room for sufficient entropy in the random portion of the UUID after the counter.
  This entropy helps improve the unguessability characteristics of UUIDs created
  within the batch.

The following sub-topics cover rollover handling with either type of counter
method:

{: vspace='0'}

Counter Rollover Guards:
: The technique from Fixed-Length Dedicated Counter Seeding which describes
  allocating a segment of the fixed-length counter as a rollover guard is also
  helpful to mitigate counter rollover issues.
  This same technique can be leveraged with Monotonic random counter methods
  by ensuring the total length of a possible increment in the least significant,
  right most position is less than the total length of the random being incremented.
  As such the most significant, left-most, bits can be incremented as rollover
  guarding.

Counter Rollover Handling:
: Counter rollovers SHOULD be handled by the application to avoid sorting issues.
  The general guidance is that applications that care about absolute monotonicity
  and sortability SHOULD freeze the counter and wait for the timestamp to advance
  which ensures monotonicity is not broken.
  Alternatively, implementations MAY increment the timestamp ahead of the actual
  time and reinitialize the counter.

Implementations MAY use the following logic to ensure UUIDs featuring embedded
counters are monotonic in nature:


1. Compare the current timestamp against the previously stored timestamp.



1. If the current timestamp is equal to the previous timestamp; increment the
  counter according to the desired method.



1. If the current timestamp is greater than the previous timestamp; re-initialize
  the desired counter method to the new timestamp and generate new random bytes
  (if the bytes were frozen or being used as the seed for a monotonic counter).



Implementations SHOULD check if the the currently generated UUID is greater
than the previously generated UUID. If this is not the case then any number
of things could have occurred. Such as, but not limited to, clock rollbacks,
leap second handling or counter rollovers. Applications SHOULD embed sufficient
logic to catch these scenarios and correct the problem ensuring the next
UUID generated is greater than the previous. To handle this scenario, the
general guidance is that application MAY reuse the previous timestamp and
increment the previous counter method.

## UUID Generator States {#generator_states}

The UUID Generator state only needs to be read from stable storage once at boot
time, if it is read into a system-wide shared volatile store (and
updated whenever the stable store is updated).

If an implementation does not have any stable store available, then
it can always say that the values were unavailable.  This is the
least desirable implementation because it will increase the frequency
of creation of values such as clock sequence, counters or random data which increases the
probability of duplicates.

For UUIDv1 and UUIDv6, if the node ID can never change (e.g., the net card is inseparable
from the system), or if any change also reinitializes the clock
sequence to a random value, then instead of keeping it in stable
store, the current node ID may be returned

For UUIDv1 and UUIDv6, the state does not always need to be written to stable store every
time a UUID is generated.  The timestamp in the stable store can be
periodically set to a value larger than any yet used in a UUID.  As
long as the generated UUIDs have timestamps less than that value, and
the clock sequence and node ID remain unchanged, only the shared
volatile copy of the state needs to be updated.  Furthermore, if the
timestamp value in stable store is in the future by less than the
typical time it takes the system to reboot, a crash will not cause a
reinitialization of the clock sequence.

If it is too expensive to access shared state each time a UUID is
generated, then the system-wide generator can be implemented to
allocate a block of time stamps each time it is called; a per-
process generator can allocate from that block until it is exhausted.

## Distributed UUID Generation {#distributed_shared_knowledge}

Some implementations MAY desire to utilize multi-node, clustered, applications
which involve two or more
nodes independently generating UUIDs that will be stored in a common location.
While UUIDs already feature sufficient entropy to ensure that the chances
of collision are low as the total number of nodes increase; so does the likelihood
of a collision.

This section will detail the approaches that have been observed by by multi-node
UUID implementations in distributed environments.

{: vspace='0'}

Centralized Registry:
: With this method all nodes tasked with creating UUIDs consult a central registry
  and confirm the generated value is unique. As applications scale the communication
  with the central registry could become a bottleneck and impact UUID generation
  in a negative way. Utilization of shared knowledge schemes with central/global
  registries is outside the scope of this specification and should generally be discouraged.

Node IDs:
: With this method, a pseudo-random Node ID value is placed within the UUID
  layout.
  This identifier helps ensure the bit-space for a given node is unique, resulting
  in UUIDs that do not conflict with any other UUID created by another node
  with a different node id.
  Implementations that choose to leverage an embedded node id SHOULD utilize
  UUIDv8.
  The node id SHOULD NOT be an IEEE 802 MAC address as per {{Security}}.
  The location and bit length are left to implementations and are outside the
  scope of this specification.
  Furthermore, the creation and negotiation of unique node ids among nodes
  is also out of scope for this specification.

Utilization of either a Centralized Registry or Node ID are not required
for implementing UUIDs in this specification. However implementations SHOULD
utilize one of the two aforementioned methods if distributed UUID generation
is a requirement.

## Name-Based UUID Generation {#name_based_uuid_generation}
TODO, define how to compute a namespace ID if I don't want to use one from {{namespaces}}

The concept of name and name space should be broadly construed, and not
limited to textual names.  For example, some name spaces are the
domain name system, URLs, Object Identifiers (OIDs), X.500 Distinguished
Names (DNs), and reserved words in a programming language.  The
mechanisms or conventions used for allocating names and ensuring
their uniqueness within their name spaces are beyond the scope of
this specification.

The requirements for these types of UUIDs are as follows:

* The UUIDs generated at different times from the same name in the
  same namespace MUST be equal.

* The UUIDs generated from two different names in the same namespace
  should be different (with very high probability).

* The UUIDs generated from the same name in two different namespaces
  should be different (with very high probability).

* If two UUIDs that were generated from names are equal, then they
  were generated from the same name in the same namespace (with very
  high probability).

## Collision Resistance {#collision_resistance}

Implementations SHOULD weigh the consequences of UUID collisions within their
application and when deciding between UUID versions that use entropy (random)
versus the other components such as {{timestamp_granularity}} and {{monotonicity_counters}}.
This is especially true for distributed node collision resistance as defined
by {{distributed_shared_knowledge}}.

There are two example scenarios below which help illustrate the varying seriousness
of a collision within an application.

{: vspace='0'}

Low Impact
: A UUID collision generated a duplicate log entry which results in incorrect
  statistics derived from the data. Implementations that are not negatively
  affected by collisions may continue with the entropy and uniqueness provided
  by the traditional UUID format.

High Impact:
: A duplicate key causes an airplane to receive the wrong course which puts
  people's lives at risk. In this scenario there is no margin for error. Collisions
  MUST be avoided and failure is unacceptable. Applications dealing with this
  type of scenario MUST employ as much collision resistance as possible within
  the given application context.


## Global and Local Uniqueness {#global_local_uniqueness}

UUIDs created by this specification MAY be used to provide local uniqueness
guarantees.
For example, ensuring UUIDs created within a local application context are
unique within a database MAY be sufficient for some implementations where
global uniqueness outside of the application context, in other applications,
or around the world is not required.

Although true global uniqueness is impossible to guarantee without a shared
knowledge scheme; a shared knowledge scheme is not required by UUID to provide
uniqueness guarantees.
Implementations MAY implement a shared knowledge scheme introduced in {{distributed_shared_knowledge}} as they see fit to extend the uniqueness guaranteed this specification.


## Unguessability {#unguessability}
TODO: Here or in security considerations, discuss security considerations with with "running out of random"

Implementations SHOULD utilize a cryptographically secure pseudo-random number
generator (CSPRNG) to provide values that are both difficult to predict ("unguessable")
and have a low likelihood of collision ("unique").
Care SHOULD be taken to ensure the CSPRNG state is properly reseeded upon
state changes, such as process forks, to ensure proper CSPRNG operation.
CSPRNG ensures the best of {{collision_resistance}} and {{Security}} are present in modern UUIDs.

Further advice on generating cryptographic-quality random numbers can be found in {{RFC4086}}

## UUIDs that Do Not Identify the Host {#unidentifiable}
This section describes how to generate a UUIDv1 or UUIDv6 value if an IEEE
802 address is not available, or its use is not desired.

One approach is to contact the IEEE and get a separate block of
addresses.  At the time of writing, the application could be found at
[](https://standards.ieee.org/products-programs/regauth/).

A better solution is to obtain a 47-bit cryptographic quality random
number and use it as the low 47 bits of the node ID, with the least
significant bit of the first octet of the node ID set to one.  This
bit is the unicast/multicast bit, which will never be set in IEEE 802
addresses obtained from network cards.  Hence, there can never be a
conflict between UUIDs generated by machines with and without network
cards.  (Recall that the IEEE 802 spec talks about transmission
order, which is the opposite of the in-memory representation that is
discussed in this document.)

For compatibility with earlier specifications, note that this
document uses the unicast/multicast bit, instead of the arguably more
correct local/global bit.

In addition, items such as the computer's name and the name of the
operating system, while not strictly speaking random, will help
differentiate the results from those obtained by other systems.

The exact algorithm to generate a node ID using these data is system
specific, because both the data available and the functions to obtain
them are often very system specific.  A generic approach, however, is
to accumulate as many sources as possible into a buffer, use a
message digest such as MD5 {{RFC1321}} or SHA-1 {{SHA1}}, take an arbitrary 6
bytes from the hash value, and set the multicast bit as described
above.

## Sorting {#sorting}

UUIDv6 and UUIDv7 are designed so that implementations that require sorting
(e.g. database indexes) SHOULD sort as opaque raw bytes, without need for
parsing or introspection.

Time ordered monotonic UUIDs benefit from greater database index locality
because the new values are near each other in the index.
As a result objects are more easily clustered together for better performance.
The real-world differences in this approach of index locality vs random data
inserts can be quite large.

UUIDs formats created by this specification SHOULD be Lexicographically sortable
while in the textual representation.

UUIDs created by this specification are crafted with big-ending byte order
(network byte order) in mind. If Little-endian style is required a custom
UUID format SHOULD be created using UUIDv8.


## Opacity {#opacity}

UUIDs SHOULD be treated as opaque values and implementations SHOULD NOT examine
the bits in a UUID to whatever extent is possible. However, where necessary,
inspectors should refer to {{variant_field}} and {{version_field}} for more information on determining UUID version and variant.


## DBMS and Database Considerations {#database_considerations}

For many applications, such as databases, storing UUIDs as text is unnecessarily
verbose, requiring 288 bits to represent 128 bit UUID values.
Thus, where feasible, UUIDs SHOULD be stored within database applications
as the underlying 128 bit binary value.

For other systems, UUIDs MAY be stored in binary form or as text, as appropriate.
The trade-offs to both approaches are as such:


* Storing as binary requires less space and may result in faster data access.



* Storing as text requires more space but may require less translation if the
  resulting text form is to be used after retrieval and thus maybe simpler
  to implement.



DBMS vendors are encouraged to provide functionality to generate and store
UUID formats defined by this specification for use as identifiers or left
parts of identifiers such as, but not limited to, primary keys, surrogate
keys for temporal databases, foreign keys included in polymorphic relationships,
and keys for key-value pairs in JSON columns and key-value databases.
Applications using a monolithic database may find using database-generated
UUIDs (as opposed to client-generate UUIDs) provides the best UUID monotonicity.
In addition to UUIDs, additional identifiers MAY be used to ensure integrity
and feedback.



# IANA Considerations {#IANA}

Per {{RFC8141}} here is the Namespace Registration Template filled out for this namespace and hereby a request to reference this document (when the final version is published) at {{URNNamespaces}}.  Note that namespace is already listed and this is a request to update that entry to reference this document.

Namespace Identifier: UUID (formal)

Version: 1

Date: 2003-10-01

Registrant: JTC 1/SC6 (ASN.1 Rapporteur Group)

Purpose: A UUID is an identifier that is unique across both space and time,
  with respect to the space of all UUIDs.  Since a UUID is a fixed
  size and contains a time field, it is possible for values to
  rollover (around A.D. 3400, depending on the specific algorithm
  used).  A UUID can be used for multiple purposes, from tagging
  objects with an extremely short lifetime, to reliably identifying
  very persistent objects across a network.

Syntax: The internal representation of a UUID is a specific sequence of
  bits in memory, as described in {{format}}.  To accurately
  represent a UUID as a URN, it is necessary to convert the bit
  sequence to a string representation.

  Each field is treated as an integer and has its value printed as a
  zero-filled hexadecimal digit string with the most significant
  digit first.  The hexadecimal values "a" through "f" are output as
  lower case characters and are case insensitive on input.

  The formal definition of the UUID string representation is
  provided by the following ABNF {{RFC5234}}:

~~~~ abnf
UUID                   = time-low "-" time-mid "-"
                         time-high-and-version "-"
                         clock-seq-and-reserved
                         clock-seq-low "-" node
time-low               = 4hexOctet
time-mid               = 2hexOctet
time-high-and-version  = 2hexOctet
clock-seq-and-reserved = hexOctet
clock-seq-low          = hexOctet
node                   = 6hexOctet
hexOctet               = hexDigit hexDigit
hexDigit =
      "0" / "1" / "2" / "3" / "4" / "5" / "6" / "7" / "8" / "9" /
      "a" / "b" / "c" / "d" / "e" / "f" /
      "A" / "B" / "C" / "D" / "E" / "F"
~~~~

  The following is an example of the string representation of a UUID as
  a URN:

  urn:uuid:f81d4fae-7dec-11d0-a765-00a0c91e6bf6

Assignment: Individual UUID values are generated based on the uniqueness properties otherwise covered in this document with version-specific considerations for each.  Mechinisms include pseudorandom number generation, cryptographic hashing and the option to use IEEE 802 MAC addresses.

Security and Privacy: The recommended generation algorithms for UUIDs per this document involve pseudorandom number generation and as such do not present additional privacy or data exposure risks beyond any such random value generated.  The use of IEEE 802 MAC addresses which may present security problems has explicitly been made optional and not recommended.

Interoperability: UUIDs, and UUID values in the form of URNs in particular,
  are opaque values the syntax as covered above has no proposed changes
  and thus no known interoperability issues.

Resolution: Since UUIDs are not globally resolvable, this is not applicable.

Documentation: This document and RFC4122. Relevant ancillary documentation: {{NCA}}{{C309}}

Additional Information: The intention here is simply to include this document
  in any applicable references at {{URNNamespaces}}. There is no intention
  to change the existing UUID URN registration.  The scope of this document
  pertains solely to the internal structure and versions of UUIDs, the
  textual format and URN registration are specifically out of scope and
  not changing as part of this update.

# Community Considerations {#community}

The use of UUIDs is extremely pervasive in computing.  They comprise
the core identifier infrastructure for many operating systems
(Microsoft Windows) and applications (the Mozilla browser) and in
many cases, become exposed to the Web in many non-standard ways.

This specification attempts to standardize that practice as openly as
possible and in a way that attempts to benefit the entire Internet.

# Security Considerations {#Security}

Do not assume that UUIDs are hard to guess; they should not be used
as security capabilities (identifiers whose mere possession grants
access), for example.  A predictable random number source will
exacerbate the situation.

Do not assume that it is easy to determine if a UUID has been
slightly transposed in order to redirect a reference to another
object.  Humans do not have the ability to easily check the integrity
of a UUID by simply glancing at it.

Distributed applications generating UUIDs at a variety of hosts must
be willing to rely on the random number source at all hosts.  If this
is not feasible, the namespace variant should be used.

MAC addresses pose inherent security risks and SHOULD not be used within
a UUID.
Instead CSPRNG data SHOULD be selected from a source with sufficient entropy
to ensure guaranteed
uniqueness among UUID generation. See {{unguessability}} for more information.

Timestamps embedded in the UUID do pose a very small attack surface. The
timestamp in conjunction with
an embedded counter does signal the order of creation for a given UUID and
it's corresponding data but
does not define anything about the data itself or the application as a whole.
If UUIDs are required for
use with any security operation within an application context in any shape
or form then UUIDv4, {{uuidv4}} SHOULD be utilized.

See {{RFC6151}} for MD5 Security Considerations and {{RFC6194}} for SHA1 security considerations.

# Acknowledgements {#Acknowledgements}

The authors gratefully acknowledge the contributions of Rich Salz,
Ben Campbell,
Ben Ramsey,
Fabio Lima,
Gonzalo Salgueiro,
Martin Thomson,
Murray S. Kucherawy,
Rick van Rein,
Rob Wilton,
Sean Leonard,
Theodore Y. Ts'o.,
Robert Kieffer,
sergeyprokhorenko,
LiosK

As well as all of those in the IETF community and on GitHub to who contributed
to the discussions which resulted in this document.

This document draws heavily on the OSF DCE specification for UUIDs.
Ted Ts'o provided helpful comments, especially on the byte ordering
section which we mostly plagiarized from a proposed wording he
supplied (all errors in that section are our responsibility,
however).

We are also grateful to the careful reading and bit-twiddling of Ralf
S. Engelschall, John Larmouth, and Paul Thorpe.  Professor Larmouth
was also invaluable in achieving coordination with ISO/IEC.


--- back

# Example Code {#example_code}

## Creating UUIDv1 through UUIDv5 Value {#sample_implementation}

This implementation consists of 5 files: uuid.h, uuid.c, sysdep.h,
sysdep.c and utest.c.  The uuid.\* files are the system independent
implementation of the UUID generation algorithms described above,
with all the optimizations described above except efficient state
sharing across processes included.  The code has been tested on Linux
(Red Hat 4.0) with GCC (2.7.2), and Windows NT 4.0 with VC++ 5.0.
The code assumes 64-bit integer support, which makes it much clearer.

All the following source files should have the following copyright
notice included:

copyrt.h

~~~

/*
** Copyright (c) 1990- 1993, 1996 Open Software Foundation, Inc.
** Copyright (c) 1989 by Hewlett-Packard Company, Palo Alto, Ca. &
** Digital Equipment Corporation, Maynard, Mass.
** Copyright (c) 1998 Microsoft.
** To anyone who acknowledges that this file is provided "AS IS"
** without any express or implied warranty: permission to use, copy,
** modify, and distribute this file for any purpose is hereby
** granted without fee, provided that the above copyright notices and
** this notice appears in all source code copies, and that none of
** the names of Open Software Foundation, Inc., Hewlett-Packard
** Company, or Digital Equipment Corporation be used in advertising
** or publicity pertaining to distribution of the software without
** specific, written prior permission. Neither Open Software
** Foundation, Inc., Hewlett-Packard Company, Microsoft, nor Digital
** Equipment Corporation makes any representations about the
** suitability of this software for any purpose.
*/

~~~

uuid.h

~~~
#include "copyrt.h"
#undef uuid_t
typedef struct {
    unsigned32  time_low;
    unsigned16  time_mid;
    unsigned16  time_hi_and_version;
    unsigned8   clock_seq_hi_and_reserved;
    unsigned8   clock_seq_low;
    byte        node[6];
} uuid_t;

/* uuid_create -- generate a UUID */
int uuid_create(uuid_t * uuid);

/* uuid_create_md5_from_name -- create a version 3 (MD5) UUID using a
   "name" from a "name space" */
void uuid_create_md5_from_name(
    uuid_t *uuid,         /* resulting UUID */
    uuid_t nsid,          /* UUID of the namespace */
    void *name,           /* the name from which to generate a UUID */
    int namelen           /* the length of the name */
);

/* uuid_create_sha1_from_name -- create a version 5 (SHA-1) UUID
   using a "name" from a "name space" */
void uuid_create_sha1_from_name(

    uuid_t *uuid,         /* resulting UUID */
    uuid_t nsid,          /* UUID of the namespace */
    void *name,           /* the name from which to generate a UUID */
    int namelen           /* the length of the name */
);

/* uuid_compare --  Compare two UUID's "lexically" and return
        -1   u1 is lexically before u2
         0   u1 is equal to u2
         1   u1 is lexically after u2
   Note that lexical ordering is not temporal ordering!
*/
int uuid_compare(uuid_t *u1, uuid_t *u2);
~~~

uuid.c

~~~
#include "copyrt.h"
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include "sysdep.h"
#include "uuid.h"

/* various forward declarations */
static int read_state(unsigned16 *clockseq, uuid_time_t *timestamp,
    uuid_node_t *node);
static void write_state(unsigned16 clockseq, uuid_time_t timestamp,
    uuid_node_t node);
static void format_uuid_v1(uuid_t *uuid, unsigned16 clockseq,
    uuid_time_t timestamp, uuid_node_t node);
static void format_uuid_v3or5(uuid_t *uuid, unsigned char hash[16],
    int v);
static void get_current_time(uuid_time_t *timestamp);
static unsigned16 true_random(void);

/* uuid_create -- generate a UUID */
int uuid_create(uuid_t *uuid)
{
     uuid_time_t timestamp, last_time;
     unsigned16 clockseq;
     uuid_node_t node;
     uuid_node_t last_node;
     int f;

     /* acquire system-wide lock so we're alone */
     LOCK;
     /* get time, node ID, saved state from non-volatile storage */
     get_current_time(&timestamp);
     get_ieee_node_identifier(&node);
     f = read_state(&clockseq, &last_time, &last_node);

     /* if no NV state, or if clock went backwards, or node ID
        changed (e.g., new network card) change clockseq */
     if (!f || memcmp(&node, &last_node, sizeof node))
         clockseq = true_random();
     else if (timestamp < last_time)
         clockseq++;

     /* save the state for next time */
     write_state(clockseq, timestamp, node);

     UNLOCK;

     /* stuff fields into the UUID */
     format_uuid_v1(uuid, clockseq, timestamp, node);
     return 1;
}

/* format_uuid_v1 -- make a UUID from the timestamp, clockseq,
                     and node ID */
void format_uuid_v1(uuid_t* uuid, unsigned16 clock_seq,
                    uuid_time_t timestamp, uuid_node_t node)
{
    /* Construct a version 1 uuid with the information we've gathered
       plus a few constants. */
    uuid->time_low = (unsigned long)(timestamp & 0xFFFFFFFF);
    uuid->time_mid = (unsigned short)((timestamp >> 32) & 0xFFFF);
    uuid->time_hi_and_version =
        (unsigned short)((timestamp >> 48) & 0x0FFF);
    uuid->time_hi_and_version |= (1 << 12);
    uuid->clock_seq_low = clock_seq & 0xFF;
    uuid->clock_seq_hi_and_reserved = (clock_seq & 0x3F00) >> 8;
    uuid->clock_seq_hi_and_reserved |= 0x80;
    memcpy(&uuid->node, &node, sizeof uuid->node);
}

/* data type for UUID generator persistent state */
typedef struct {
    uuid_time_t  ts;       /* saved timestamp */
    uuid_node_t  node;     /* saved node ID */
    unsigned16   cs;       /* saved clock sequence */
} uuid_state;

static uuid_state st;

/* read_state -- read UUID generator state from non-volatile store */
int read_state(unsigned16 *clockseq, uuid_time_t *timestamp,
               uuid_node_t *node)
{
    static int inited = 0;
    FILE *fp;

    /* only need to read state once per boot */
    if (!inited) {
        fp = fopen("state", "rb");
        if (fp == NULL)
            return 0;
        fread(&st, sizeof st, 1, fp);
        fclose(fp);
        inited = 1;
    }
    *clockseq = st.cs;
    *timestamp = st.ts;
    *node = st.node;
    return 1;
}

/* write_state -- save UUID generator state back to non-volatile
   storage */
void write_state(unsigned16 clockseq, uuid_time_t timestamp,
                 uuid_node_t node)
{
    static int inited = 0;
    static uuid_time_t next_save;
    FILE* fp;

    if (!inited) {
        next_save = timestamp;
        inited = 1;
    }

    /* always save state to volatile shared state */
    st.cs = clockseq;
    st.ts = timestamp;
    st.node = node;
    if (timestamp >= next_save) {
        fp = fopen("state", "wb");
        fwrite(&st, sizeof st, 1, fp);
        fclose(fp);
        /* schedule next save for 10 seconds from now */
        next_save = timestamp + (10 * 10 * 1000 * 1000);
    }
}

/* get-current_time -- get time as 60-bit 100ns ticks since UUID epoch.
   Compensate for the fact that real clock resolution is
   less than 100ns. */
void get_current_time(uuid_time_t *timestamp)
{
    static int inited = 0;
    static uuid_time_t time_last;
    static unsigned16 uuids_this_tick;
    uuid_time_t time_now;

    if (!inited) {
        get_system_time(&time_now);
        uuids_this_tick = UUIDS_PER_TICK;
        inited = 1;
    }

    for ( ; ; ) {
        get_system_time(&time_now);

        /* if clock reading changed since last UUID generated, */
        if (time_last != time_now) {
            /* reset count of uuids gen'd with this clock reading */
            uuids_this_tick = 0;
            time_last = time_now;
            break;
        }
        if (uuids_this_tick < UUIDS_PER_TICK) {
            uuids_this_tick++;
            break;
        }

        /* going too fast for our clock; spin */
    }
    /* add the count of uuids to low order bits of the clock reading */
    *timestamp = time_now + uuids_this_tick;
}

/* true_random -- generate a crypto-quality random number.
   **This sample doesn't do that.** */
static unsigned16 true_random(void)
{
    static int inited = 0;
    uuid_time_t time_now;

    if (!inited) {
        get_system_time(&time_now);
        time_now = time_now / UUIDS_PER_TICK;
        srand((unsigned int)
               (((time_now >> 32) ^ time_now) & 0xffffffff));
        inited = 1;
    }

    return rand();
}

/* uuid_create_md5_from_name -- create a version 3 (MD5) UUID using a
   "name" from a "name space" */
void uuid_create_md5_from_name(uuid_t *uuid, uuid_t nsid, void *name,
                               int namelen)
{
    MD5_CTX c;
    unsigned char hash[16];
    uuid_t net_nsid;

    /* put name space ID in network byte order so it hashes the same
       no matter what endian machine we're on */
    net_nsid = nsid;
    net_nsid.time_low = htonl(net_nsid.time_low);
    net_nsid.time_mid = htons(net_nsid.time_mid);
    net_nsid.time_hi_and_version = htons(net_nsid.time_hi_and_version);

    MD5Init(&c);
    MD5Update(&c, &net_nsid, sizeof net_nsid);
    MD5Update(&c, name, namelen);
    MD5Final(hash, &c);

    /* the hash is in network byte order at this point */
    format_uuid_v3or5(uuid, hash, 3);
}

void uuid_create_sha1_from_name(uuid_t *uuid, uuid_t nsid, void *name,
                                int namelen)
{
    SHA_CTX c;
    unsigned char hash[20];
    uuid_t net_nsid;

    /* put name space ID in network byte order so it hashes the same
       no matter what endian machine we're on */
    net_nsid = nsid;
    net_nsid.time_low = htonl(net_nsid.time_low);
    net_nsid.time_mid = htons(net_nsid.time_mid);
    net_nsid.time_hi_and_version = htons(net_nsid.time_hi_and_version);

    SHA1_Init(&c);
    SHA1_Update(&c, &net_nsid, sizeof net_nsid);
    SHA1_Update(&c, name, namelen);
    SHA1_Final(hash, &c);

    /* the hash is in network byte order at this point */
    format_uuid_v3or5(uuid, hash, 5);
}

/* format_uuid_v3or5 -- make a UUID from a (pseudo)random 128-bit
   number */
void format_uuid_v3or5(uuid_t *uuid, unsigned char hash[16], int v)
{
    /* convert UUID to local byte order */
    memcpy(uuid, hash, sizeof *uuid);
    uuid->time_low = ntohl(uuid->time_low);
    uuid->time_mid = ntohs(uuid->time_mid);
    uuid->time_hi_and_version = ntohs(uuid->time_hi_and_version);

    /* put in the variant and version bits */
    uuid->time_hi_and_version &= 0x0FFF;
    uuid->time_hi_and_version |= (v << 12);
    uuid->clock_seq_hi_and_reserved &= 0x3F;
    uuid->clock_seq_hi_and_reserved |= 0x80;
}

/* uuid_compare --  Compare two UUID's "lexically" and return */
#define CHECK(f1, f2) if (f1 != f2) return f1 < f2 ? -1 : 1;
int uuid_compare(uuid_t *u1, uuid_t *u2)
{
    int i;

    CHECK(u1->time_low, u2->time_low);
    CHECK(u1->time_mid, u2->time_mid);
    CHECK(u1->time_hi_and_version, u2->time_hi_and_version);
    CHECK(u1->clock_seq_hi_and_reserved, u2->clock_seq_hi_and_reserved);
    CHECK(u1->clock_seq_low, u2->clock_seq_low)
    for (i = 0; i < 6; i++) {
        if (u1->node[i] < u2->node[i])
            return -1;
        if (u1->node[i] > u2->node[i])
            return 1;
    }
    return 0;
}
#undef CHECK
~~~

sysdep.h

~~~

#include "copyrt.h"
/* remove the following define if you aren't running WIN32 */
#define WININC 0

#ifdef WININC
#include <windows.h>
#else
#include <sys/types.h>
#include <sys/time.h>
#include <sys/sysinfo.h>
#endif

#include "global.h"
/* change to point to where MD5 .h's live; RFC 1321 has sample
   implementation */
#include "md5.h"

/* set the following to the number of 100ns ticks of the actual
   resolution of your system's clock */
#define UUIDS_PER_TICK 1024

/* Set the following to a calls to get and release a global lock */
#define LOCK
#define UNLOCK

typedef unsigned long   unsigned32;
typedef unsigned short  unsigned16;
typedef unsigned char   unsigned8;
typedef unsigned char   byte;

/* Set this to what your compiler uses for 64-bit data type */
#ifdef WININC
#define unsigned64_t unsigned __int64
#define I64(C) C
#else
#define unsigned64_t unsigned long long
#define I64(C) C##LL
#endif

typedef unsigned64_t uuid_time_t;
typedef struct {
    char nodeID[6];
} uuid_node_t;

void get_ieee_node_identifier(uuid_node_t *node);
void get_system_time(uuid_time_t *uuid_time);
void get_random_info(char seed[16]);
~~~

sysdep.c

~~~
#include "copyrt.h"
#include <stdio.h>
#include "sysdep.h"

/* system dependent call to get IEEE node ID.
   This sample implementation generates a random node ID. */
void get_ieee_node_identifier(uuid_node_t *node)
{
    static inited = 0;
    static uuid_node_t saved_node;
    char seed[16];
    FILE *fp;

    if (!inited) {
        fp = fopen("nodeid", "rb");
        if (fp) {
            fread(&saved_node, sizeof saved_node, 1, fp);
            fclose(fp);
        }
        else {
            get_random_info(seed);
            seed[0] |= 0x01;
            memcpy(&saved_node, seed, sizeof saved_node);
            fp = fopen("nodeid", "wb");
            if (fp) {
                fwrite(&saved_node, sizeof saved_node, 1, fp);
                fclose(fp);
            }
        }
        inited = 1;
    }

    *node = saved_node;
}

/* system dependent call to get the current system time. Returned as
   100ns ticks since UUID epoch, but resolution may be less than
   100ns. */
#ifdef _WINDOWS_

void get_system_time(uuid_time_t *uuid_time)
{
    ULARGE_INTEGER time;

    /* NT keeps time in FILETIME format which is 100ns ticks since
       Jan 1, 1601. UUIDs use time in 100ns ticks since Oct 15, 1582.
       The difference is 17 Days in Oct + 30 (Nov) + 31 (Dec)
       + 18 years and 5 leap days. */
    GetSystemTimeAsFileTime((FILETIME *)&time);
    time.QuadPart +=

          (unsigned __int64) (1000*1000*10)       // seconds
        * (unsigned __int64) (60 * 60 * 24)       // days
        * (unsigned __int64) (17+30+31+365*18+5); // # of days
    *uuid_time = time.QuadPart;
}

/* Sample code, not for use in production; see RFC 4086 */
void get_random_info(char seed[16])
{
    MD5_CTX c;
    struct {
        MEMORYSTATUS m;
        SYSTEM_INFO s;
        FILETIME t;
        LARGE_INTEGER pc;
        DWORD tc;
        DWORD l;
        char hostname[MAX_COMPUTERNAME_LENGTH + 1];
    } r;

    MD5Init(&c);
    GlobalMemoryStatus(&r.m);
    GetSystemInfo(&r.s);
    GetSystemTimeAsFileTime(&r.t);
    QueryPerformanceCounter(&r.pc);
    r.tc = GetTickCount();
    r.l = MAX_COMPUTERNAME_LENGTH + 1;
    GetComputerName(r.hostname, &r.l);
    MD5Update(&c, &r, sizeof r);
    MD5Final(seed, &c);
}

#else

void get_system_time(uuid_time_t *uuid_time)
{
    struct timeval tp;

    gettimeofday(&tp, (struct timezone *)0);

    /* Offset between UUID formatted times and Unix formatted times.
       UUID UTC base time is October 15, 1582.
       Unix base time is January 1, 1970.*/
    *uuid_time = ((unsigned64)tp.tv_sec * 10000000)
        + ((unsigned64)tp.tv_usec * 10)
        + I64(0x01B21DD213814000);
}

/* Sample code, not for use in production; see RFC 4086 */
void get_random_info(char seed[16])
{
    MD5_CTX c;
    struct {
        struct sysinfo s;
        struct timeval t;
        char hostname[257];
    } r;

    MD5Init(&c);
    sysinfo(&r.s);
    gettimeofday(&r.t, (struct timezone *)0);
    gethostname(r.hostname, 256);
    MD5Update(&c, &r, sizeof r);
    MD5Final(seed, &c);
}

#endif
~~~

utest.c

~~~
#include "copyrt.h"
#include "sysdep.h"
#include <stdio.h>
#include "uuid.h"

uuid_t NameSpace_DNS = { /* 6ba7b810-9dad-11d1-80b4-00c04fd430c8 */
    0x6ba7b810,
    0x9dad,
    0x11d1,
    0x80, 0xb4, 0x00, 0xc0, 0x4f, 0xd4, 0x30, 0xc8
};

/* puid -- print a UUID */
void puid(uuid_t u)
{
    int i;

    printf("%8.8x-%4.4x-%4.4x-%2.2x%2.2x-", u.time_low, u.time_mid,
    u.time_hi_and_version, u.clock_seq_hi_and_reserved,
    u.clock_seq_low);
    for (i = 0; i < 6; i++)
        printf("%2.2x", u.node[i]);
    printf("\n");
}

/* Simple driver for UUID generator */
void main(int argc, char **argv)
{
    uuid_t u;
    int f;

    uuid_create(&u);
    printf("uuid_create(): "); puid(u);

    f = uuid_compare(&u, &u);
    printf("uuid_compare(u,u): %d\n", f);     /* should be 0 */
    f = uuid_compare(&u, &NameSpace_DNS);
    printf("uuid_compare(u, NameSpace_DNS): %d\n", f); /* s.b. 1 */
    f = uuid_compare(&NameSpace_DNS, &u);
    printf("uuid_compare(NameSpace_DNS, u): %d\n", f); /* s.b. -1 */
    uuid_create_md5_from_name(&u, NameSpace_DNS, "www.example.com", 15);
    printf("uuid_create_md5_from_name(): "); puid(u);
}
~~~

Sample Output of utest
~~~
     uuid_create(): 7d444840-9dc0-11d1-b245-5ffdce74fad2
     uuid_compare(u,u): 0
     uuid_compare(u, NameSpace_DNS): 1
     uuid_compare(NameSpace_DNS, u): -1
     uuid_create_md5_from_name(): 5df41881-3aed-3515-88a7-2f4a814cf09e
~~~

## Some Name Space IDs {#namespaces}

   This appendix lists the name space IDs for some potentially
   interesting name spaces, as initialized C structures and in the
   string representation defined above.

~~~
   /* Name string is a fully-qualified domain name */
   uuid_t NameSpace_DNS = { /* 6ba7b810-9dad-11d1-80b4-00c04fd430c8 */
       0x6ba7b810,
       0x9dad,
       0x11d1,
       0x80, 0xb4, 0x00, 0xc0, 0x4f, 0xd4, 0x30, 0xc8
   };

   /* Name string is a URL */
   uuid_t NameSpace_URL = { /* 6ba7b811-9dad-11d1-80b4-00c04fd430c8 */
       0x6ba7b811,
       0x9dad,
       0x11d1,
       0x80, 0xb4, 0x00, 0xc0, 0x4f, 0xd4, 0x30, 0xc8
   };

   /* Name string is an ISO OID */
   uuid_t NameSpace_OID = { /* 6ba7b812-9dad-11d1-80b4-00c04fd430c8 */
       0x6ba7b812,
       0x9dad,
       0x11d1,
       0x80, 0xb4, 0x00, 0xc0, 0x4f, 0xd4, 0x30, 0xc8
   };

   /* Name string is an X.500 DN (in DER or a text output format) */
   uuid_t NameSpace_X500 = { /* 6ba7b814-9dad-11d1-80b4-00c04fd430c8 */
       0x6ba7b814,
       0x9dad,
       0x11d1,
       0x80, 0xb4, 0x00, 0xc0, 0x4f, 0xd4, 0x30, 0xc8
   };
~~~

## Creating a UUIDv6 Value {#creating_a_uuidv6_value}

This section details a function in C which converts from a UUID version 1
to version 6:


~~~~
#include <stdio.h>
#include <stdint.h>
#include <inttypes.h>
#include <arpa/inet.h>
#include <uuid/uuid.h>

/* Converts UUID version 1 to version 6 in place. */
void uuidv1tov6(uuid_t u) {

  uint64_t ut;
  unsigned char *up = (unsigned char *)u;

  // load ut with the first 64 bits of the UUID
  ut = ((uint64_t)ntohl(*((uint32_t*)up))) << 32;
  ut |= ((uint64_t)ntohl(*((uint32_t*)&up[4])));

  // dance the bit-shift...
  ut =
    ((ut >> 32) & 0x0FFF) | // 12 least significant bits
    (0x6000) | // version number
    ((ut >> 28) & 0x0000000FFFFF0000) | // next 20 bits
    ((ut << 20) & 0x000FFFF000000000) | // next 16 bits
    (ut << 52); // 12 most significant bits

  // store back in UUID
  *((uint32_t*)up) = htonl((uint32_t)(ut >> 32));
  *((uint32_t*)&up[4]) = htonl((uint32_t)(ut));

}
~~~~
{: title='UUIDv6 Function in C'}


## Creating a UUIDv7 Value {#creating_a_uuidv7_value}


~~~~
#include <stdio.h>
#include <stdlib.h>
#include <stdint.h>
#include <string.h>
#include <time.h>

// ...

// csprng data source
FILE *rndf;
rndf = fopen("/dev/urandom", "r");
if (rndf == 0) {
    printf("fopen /dev/urandom error\n");
    return 1;
}

// ...

// generate one UUIDv7E
uint8_t u[16];
struct timespec ts;
int ret;

ret = clock_gettime(CLOCK_REALTIME, &ts);
if (ret != 0) {
    printf("clock_gettime error: %d\n", ret);
    return 1;
}

uint64_t tms;

tms = ((uint64_t)ts.tv_sec) * 1000;
tms += ((uint64_t)ts.tv_nsec) / 1000000;

memset(u, 0, 16);

fread(&u[6], 10, 1, rndf); // fill everything after the timestamp with random bytes

*((uint64_t*)(u)) |= htonll(tms << 16); // shift time into first 48 bits and OR into place

u[8] = 0x80 | (u[8] & 0x3F); // set variant field, top two bits are 1, 0
u[6] = 0x70 | (u[6] & 0x0F); // set version field, top four bits are 0, 1, 1, 1
~~~~
{: title='UUIDv7 Function in C'}


## Creating a UUIDv8 Value {#creating_a_uuidv8_value}

UUIDv8 will vary greatly from implementation to implementation.

The following example utilizes:


* 32 bit custom-epoch timestamp (seconds elapsed since 2020-01-01 00:00:00
  UTC)



* 16 bit exotic resolution (~15 microsecond) subsecond timestamp encoded using
  the fractional representation



* 58 bit random number



* 8 bit application-specific unique node ID



* 8 bit rolling sequence number




~~~~
#include <stdint.h>
#include <time.h>

int get_random_bytes(uint8_t *buffer, int count) {
  // ...
}

int generate_uuidv8(uint8_t *uuid, uint8_t node_id) {
  struct timespec tp;
  if (clock_gettime(CLOCK_REALTIME, &tp) != 0)
    return -1; // real-time clock error

  // 32 bit biased timestamp (seconds elapsed since 2020-01-01 00:00:00 UTC)
  uint32_t timestamp_sec = tp.tv_sec - 1577836800;
  uuid[0] = timestamp_sec >> 24;
  uuid[1] = timestamp_sec >> 16;
  uuid[2] = timestamp_sec >> 8;
  uuid[3] = timestamp_sec;

  // 16 bit subsecond fraction (~15 microsecond resolution)
  uint16_t timestamp_subsec = ((uint64_t)tp.tv_nsec << 16) / 1000000000;
  uuid[4] = timestamp_subsec >> 8;
  uuid[5] = timestamp_subsec;

  // 58 bit random number and required ver and var fields
  if (get_random_bytes(&uuid[6], 8) != 0)
    return -1; // random number generator error
  uuid[6] = 0x80 | (uuid[6] & 0x0f);
  uuid[8] = 0x80 | (uuid[8] & 0x3f);

  // 8 bit application-specific node ID to guarantee application-wide uniqueness
  uuid[14] = node_id;

  // 8 bit rolling sequence number to help ensure process-wide uniqueness
  static uint8_t sequence = 0;
  uuid[15] = sequence++; // NOTE: unprotected from race conditions

  return 0;
}
~~~~
{: title='UUIDv8 Function in C'}

# Test Vectors {#test_vectors}

Both UUIDv1 and UUIDv6 test vectors utilize the same 60 bit timestamp: 0x1EC9414C232AB00
(138648505420000000) Tuesday, February 22, 2022 2:22:22.000000 PM GMT-05:00

Both UUIDv1 and UUIDv6 utilize the same values in clk_seq_hi_res, clock_seq_low,
and node. All of which have been generated with random data.


~~~~
# Unix Nanosecond precision to Gregorian 100-nanosecond intervals
gregorian_100_ns = (Unix_64_bit_nanoseconds / 100) + gregorian_Unix_offset

# Gregorian to Unix Offset:
# The number of 100-ns intervals between the
# UUID epoch 1582-10-15 00:00:00 and the Unix epoch 1970-01-01 00:00:00.
# gregorian_Unix_offset = 0x01b21dd213814000 or 122192928000000000

# Unix 64 bit Nanosecond Timestamp:
# Unix NS: Tuesday, February 22, 2022 2:22:22 PM GMT-05:00
# Unix_64_bit_nanoseconds = 0x16D6320C3D4DCC00 or 1645557742000000000

# Work:
# gregorian_100_ns = (1645557742000000000 / 100) + 122192928000000000
# (138648505420000000 - 122192928000000000) * 100 = Unix_64_bit_nanoseconds

# Final:
# gregorian_100_ns = 0x1EC9414C232AB00 or 138648505420000000

# Original: 000111101100100101000001010011000010001100101010101100000000
# UUIDv1:   11000010001100101010101100000000|1001010000010100|0001|000111101100
# UUIDv6:   00011110110010010100000101001100|0010001100101010|0110|101100000000
~~~~
{: title='Test Vector Timestamp Pseudo-code'}

## Example of UUIDv1 Value {#uuidv1_example}
~~~~
----------------------------------------------
field                 bits    value
----------------------------------------------
time_low              32      0xC232AB00
time_mid              16      0x9414
time_hi_and_version   16      0x11EC
clk_seq_hi_res         8      0xB3
clock_seq_low          8      0xC8
node                  48      0x9E6BDECED846
----------------------------------------------
total                128
----------------------------------------------
final_hex: C232AB00-9414-11EC-B3C8-9E6BDECED846
~~~~
{: title='UUIDv1 Example Test Vector'}

## Example of UUIDv3 Value {#uuidv3_example}
The MD5 computation from {{sample_implementation}} is detailed in {{v3md5}}
while the field mapping and all values are illustrated in {{v3fields}}.
Finally to further illustrate the bit swaping for version and variant see {{v3vervar}}.

~~~~
Name Space (DNS):       6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:                   www.example.com
-----------------------------------------------
MD5:                    5df418813aed051548a72f4a814cf09e
~~~~
{: id='v3md5' title='UUIDv3 Example MD5'}

~~~~
-------------------------------
field      bits    value
-------------------------------
md5_high   48      0x5df418813aed
ver         4      0x3
md5_mid    12      0x515
var         2      b10
md5_low    62      b00, 0x8a72f4a814cf09e
-------------------------------
total     128
-------------------------------
final: 5df41881-3aed-3515-88a7-2f4a814cf09e
~~~~
{: id='v3fields' title='UUIDv3 Example Test Vector'}

~~~~
MD5 hex and dash:       5df41881-3aed-0515-48a7-2f4a814cf09e
Ver and Var Overwrite:  xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                  5df41881-3aed-3515-88a7-2f4a814cf09e
~~~~
{: id='v3vervar' title='UUIDv3 Example Ver Var bit swaps'}

## Example of UUIDv4 Value {#uuidv4_example}
This UUIDv4 example was created by generating 16 bytes
of random data resulting in the hex value of
919108F752D133205BACF847DB4148A8. This is then used to
fill out the feilds as shown in {{v4fields}}.

Finally to further illustrate the bit swapping for version and variant see {{v4vervar}}.

~~~~
-------------------------------
field      bits    value
-------------------------------
random_a   48      0x919108f752d1
ver         4      0x4
random_b   12      0x320
var         2      b10
random_c   62      b01, 0xbacf847db4148a8
-------------------------------
total      128
-------------------------------
final: 919108f7-52d1-4320-9bac-f847db4148a8
~~~~
{: id='v4fields' title='UUIDv4 Example Test Vector'}

~~~~
Random hex:             919108f752d133205bacf847db4148a8
Random hex and dash:    919108f7-52d1-3320-5bac-f847db4148a8
Ver and Var Overwrite:  xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                  919108f7-52d1-4320-9bac-f847db4148a8
~~~~
{: id='v4vervar' title='UUIDv4 Example Ver/Var bit swaps '}


## Example of UUIDv5 Value {#uuidv5_example}
The SHA1 computation from {{sample_implementation}} is detailed in {{v5sha1}}
while the field mapping and all values are illustrated in {{v5fields}}.
Finally to further illustrate the bit swapping for version and variant and the unused/discarded part of the SHA1 value see {{v5vervar}}.

~~~~
Name Space (DNS):       6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:                   www.example.com
-----------------------------------------------
SHA1:                   2ed6657de927468b55e12665a8aea6a22dee3e35
~~~~
{: id='v5sha1' title='UUIDv5 Example SHA1'}

~~~~
-------------------------------
field      bits    value
-------------------------------
sha_high   48      0x2ed6657de927
ver         4      0x5
sha_mid    12      0x68b
var         2      b10
sha_low    62      b01, 0x5e12665a8aea6a2
-------------------------------
total     128
-------------------------------
final: 2ed6657d-e927-568b-95e1-2665a8aea6a2
~~~~
{: id='v5fields' title='UUIDv5 Example Test Vector'}

~~~~
SHA1 hex and dash:      2ed6657d-e927-468b-55e1-2665a8aea6a2-2dee3e35
Ver and Var Overwrite:  xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                  2ed6657d-e927-568b-95e1-2665a8aea6a2
Discarded:                                                  -2dee3e35
~~~~
{: id='v5vervar' title='UUIDv5 Example Ver/Var bit swaps and discarded SHA1 segment'}

## Example of a UUIDv6 Value {#uuidv6_example}

~~~~
-----------------------------------------------
field                 bits    value
-----------------------------------------------
time_high              32     0x1EC9414C
time_mid               16     0x232A
time_low_and_version   16     0x6B00
clk_seq_hi_res          8     0xB3
clock_seq_low           8     0xC8
node                   48     0x9E6BDECED846
-----------------------------------------------
total                 128
-----------------------------------------------
final_hex: 1EC9414C-232A-6B00-B3C8-9E6BDECED846
~~~~
{: title='UUIDv6 Example Test Vector'}


## Example of a UUIDv7 Value {#uuidv7_example}

This example UUIDv7 test vector utilizes a well-known 32 bit Unix epoch with
additional millisecond precision to fill the first 48 bits

rand_a and rand_b are filled with random data.

The timestamp is Tuesday, February 22, 2022 2:22:22.00 PM GMT-05:00 represented
as 0x17F22E279B0 or 1645557742000


~~~~
-------------------------------
field      bits    value
-------------------------------
unix_ts_ms   48    0x17F22E279B0
ver           4    0x7
rand_a       12    0xCC3
var           2    b10
rand_b       62    b01, 0x8C4DC0C0C07398F
-------------------------------
total       128
-------------------------------
final: 017F22E2-79B0-7CC3-98C4-DC0C0C07398F
~~~~
{: title='UUIDv7 Example Test Vector'}


## Example of a UUIDv8 Value {#uuidv8_example}

This example UUIDv8 test vector utilizes a well-known 64 bit Unix epoch with
nanosecond precision, truncated to the least-significant, right-most, bits
to fill the first 48 bits through version.

The next two segments of custom_b and custom_c are are filled with random
data.

Timestamp is Tuesday, February 22, 2022 2:22:22.000000 PM GMT-05:00 represented
as 0x16D6320C3D4DCC00 or 1645557742000000000

It should be noted that this example is just to illustrate one scenario for
UUIDv8. Test vectors will likely be implementation specific and vary greatly
from this simple example.


~~~~
-------------------------------
field      bits    value
-------------------------------
custom_a     48    0x320C3D4DCC00
ver           4    0x8
custom_b     12    0x75B
var           2    b10
custom_c     62    b00, 0xEC932D5F69181C0
-------------------------------
total       128
-------------------------------
final: 320C3D4D-CC00-875B-8EC9-32D5F69181C0
~~~~
{: title='UUIDv8 Example Test Vector'}
