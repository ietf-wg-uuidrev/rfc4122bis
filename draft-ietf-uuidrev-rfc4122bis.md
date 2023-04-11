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
date: 2023

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
  RFC4122: RFC4122
  RFC8141: RFC8141
  RFC5234: RFC5234
  RFC6194: RFC6194
  SHA1:
    target: https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf
    title: Secure Hash Standard
    author:
    - org: National Institute of Standards and Technology
    date: August 2015
    seriesinfo:
      FIPS: PUB 180-4
  SHA3:
    target: https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.202.pdf
    title: "SHA-3 Standard: Permutation-Based Hash and Extendable-Output Functions"
    author:
    - org: National Institute of Standards and Technology
    date: August 2015
    seriesinfo:
      FIPS: PUB 202
  C311:
    target: https://pubs.opengroup.org/onlinepubs/9696989899/toc.pdf
    title: "DCE 1.1: Authentication and Security Services"
    rc: Open Group CAE Specification C311
    date: 1997
  RANDOM:
    target: https://peteroupc.github.io/random.html
    title: "Random Number Generator Recommendations for Applications"
    author:
    - name: Peter Occil
    date: 2023
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
UUIDs (Universally Unique IDentifiers), also known as GUIDs (Globally
Unique IDentifiers).  A UUID is 128 bits long, and can guarantee
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
UUIDs (Universally Unique IDentifiers), also known as GUIDs (Globally
Unique IDentifiers).  A UUID is 128 bits long, and requires no central
registration process.

The information here is meant to be a concise guide for those wishing
to implement services using UUIDs as URNs {{RFC8141}}.  Nothing in this document
should be construed to override the DCE standards that defined UUIDs.

There is an ITU-T Recommendation and an ISO/IEC Standard {{X667}} that are
derived from {{RFC4122}}.  Both sets of
specifications have been aligned and are fully technically
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

UUIDs are of a fixed size (128 bits), which is reasonably small
compared to other alternatives.  This lends itself well to sorting,
ordering, and hashing of all sorts, storing in databases, simple
allocation, and ease of programming in general.

Since UUIDs are unique and persistent, they make excellent Uniform
Resource Names.  The unique ability to generate a new UUID without a
registration process allows for UUIDs to be one of the URNs with the
lowest minting cost.

## Update motivation

Many things have changed in the time since UUIDs were originally created.
Modern applications have a need to create and utilize UUIDs as the primary
identifier for a variety of different items in complex computational systems,
including but not limited to database keys, file names, machine or system
names, and identifiers for event-driven transactions.

One area in which UUIDs have gained popularity is as database keys.
This stems from the increasingly distributed nature of modern applications.
In such cases, "auto increment" schemes often used by databases do not work
well, as the effort required to coordinate sequential numeric identifiers across
a network can easily become a burden.
The fact that UUIDs can be used to create unique, reasonably short values
in distributed systems without requiring coordination makes them a good
alternative, but UUID versions 1-5 lack certain other desirable characteristics:


1. Non-time-ordered UUID versions such as UUIDv4 (described in {{uuidv4}}) have poor database index
  locality.
  This means that new values created in succession are not close to each other in
  the index and thus require inserts to be performed at random
  locations.
  The negative performance effects of which on common structures used for
  this (B-tree and its variants) can be dramatic.

1. The 100-nanosecond Gregorian epoch used in UUIDv1 (described in {{uuidv1}}) timestamps is uncommon
  and difficult to represent accurately using a standard number format such
  as {{IEEE754}}.



1. Introspection/parsing is required to order by time sequence, as opposed to
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
  of a UUID versus an application that simply stores one, which are often
  different.



Due to the aforementioned issues, many widely distributed database applications
and large application vendors have sought to solve the problem of creating
a better
time-based, sortable unique identifier for use as a database key. This has
lead to numerous implementations
over the past 10+ years solving the same problem in slightly different ways.

While preparing this specification, the following 16 different implementations
were analyzed for trends in total ID length, bit layout, lexical formatting/encoding,
timestamp type, timestamp format, timestamp accuracy, node format/components,
collision handling and multi-timestamp tick generation sequencing:


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

draft-03

{: spacing="compact"}

- Revised IANA Considerations


draft-02

{: spacing="compact"}

- Change md5_high in SHA1 section to sha1_mid #59
- Describe Nil/Max UUID in variant table #16
- Further Clarify that non-descript node IDs are the preferred method in distributed UUID Generation #49
- Appendix B, consistent naming #55
- Remove duplicate ABNF from IANA considerations #56
- Monotonic Error Checking missing newline #57
- More Security Considerations Randomness #26
- SHA256 UUID Generation #50
- Expand multiplexed fields within v1 and v6 bit definitions # 43
- Clean up text in UUIDs that Do Not Identify the Host #61
- Revise UUID Generator States section #47
- Expand upon why unix epoch rollover is not a problem #44
- Delete Sample Code Appendix #62

draft-01

{: spacing="compact"}

- Mixed Case Spelling error #18
- Add "UUIDs that Do Not Identify the Host as well" reference to security considerations #19
- Out of Place Distributed node text #20
- v6 clock_seq and node usage ambiguity #21
- Figure 2 and 3 Fix Title #22
- Move Namespace Registration Template to IANA Considerations #23
- Verify ABNF formatting against RFC5234 #24
- Bump ABNF reference to RFC 5234 #25
- Modify v8 SHOULD NOT to MUST NOT #27
- Remove "time-based" constraint from version 8 UUID #29
- Further clarify v7 field description #125 #30
- Typo: Section 4.2, Version Field, "UUID from in this" #33
- Create better ABNF to represent Hex Digit #39
- Break Binary form of UUID into two lines. #40
- Move octet text from section 4 to section 5 #41
- Add forward reference to UUIDv1 and UUIDv4 in Section 2 #42
- Erronous reference to v1 in monotonicity #45
- Add Label for "Monotonic Error Checking" paragraph to frame the topic #46
- Remove IEEE paragraph from "uuids that do not identify the host" #48
- Grammar Review #52

draft-00

{: spacing="compact"}
- Merge RFC4122 with draft-peabody-dispatch-new-uuid-format-04.md
- Change: Reference RFC1321 to RFC6151
- Change: Reference RFC2141 to RFC8141
- Change: Reference RFC2234 to RFC5234
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
bits described in the next sections in determine finer structure. While discussing UUID formats and layout, bit definitions start at 0 and end at 127 while octet definitions start at 0 and end at 15.

UUIDs MAY be represented as binary data or integers.
When in use with URNs or applications, any given UUID SHOULD
be represented by the "hex-and-dash" string format consisting of multiple
groups of upper or lowercase alphanumeric hex characters separated by single dashes/hyphens.
When used with databases please refer to {{database_considerations}}.

The formal definition of the UUID string representation is provided by the following (ABNF) {{RFC5234}}.

~~~~ abnf
   UUID     = 4hexOctet "-"
              2hexOctet "-"
              2hexOctet "-"
              2hexOctet "-"
              6hexOctet
   hexOctet = HEXDIG HEXDIG
   DIGIT    = %x30-39
   HEXDIG   = DIGIT / "A" / "B" / "C" / "D" / "E" / "F"
~~~~

An example UUID using this textual representation from the above ABNF is shown in {{sampleStringUUID}}.
Note that in this example the alphabetic characters may be all uppercase, all lowercase or mixed case as per {{RFC5234, Section 2.3}}

~~~~
f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleStringUUID title='Example String UUID format'}

The same UUID from {{sampleStringUUID}} is represented in Binary {{sampleBinaryUUID}}, Integer {{sampleIntegerUUID}} and as a URN {{sampleURNUUID}} defined by {{RFC8141}}.

~~~~
111110000001110101001111101011100111110111101100000100011101000\
01010011101100101000000001010000011001001000111100110101111110110
~~~~
{: #sampleBinaryUUID title='Example Binary UUID'}

~~~~
329800735698586629295641978511506172918
~~~~
{: #sampleIntegerUUID title='Example Integer UUID'}

~~~~
urn:uuid:f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleURNUUID title='Example URN UUID'}

## Variant Field {#variant_field}

The variant field determines the layout of the UUID.  That is, the
interpretation of all other bits in the UUID depends on the setting
of the bits in the variant field.  As such, it could more accurately
be called a type field; we retain the original term for
compatibility.  The variant field consists of a variable number of
the most significant bits of octet 8 of the UUID.

{{table1}} lists the contents of the variant field, where
the letter "x" indicates a "don't-care" value.

| Msb0 | Msb1 | Msb2 | Description                                                                    |
|    0 |    x | x    | Reserved, NCS backward compatibility and includes Nil UUID as per {{niluuid}}. |
|    1 |    0 | x    | The variant specified in this document.                                        |
|    1 |    1 | 0    | Reserved, Microsoft Corporation backward compatibility.                        |
|    1 |    1 | 1    | Reserved for future definition and includes Max UUID as per {{maxuuid}}.       |
{: #table1 title='UUID Variants'}

Interoperability, in any form, with variants other than the one
defined here is not guaranteed but is not likely to be an issue in
practice.

Specifically for UUIDs in this document bits 64 and 65 of the UUID (bits 0 and 1 of octet 8) MUST be set to 1 and 0 as specified in row 2 of {{table1}}.
Accordingly, all bit and field layouts avoid the use of these bits.

## Version Field {#version_field}
The version number is in the most significant 4 bits of octet 6
(bits 48 through 51 of the UUID).

{{table2}} lists all of the versions for this UUID variant specified in this document.

| Msb0 | Msb1 | Msb2 | Msb3 | Version | Description                                                                   |
|    0 |    0 |    0 |    0 |       0 | Unused                                                                        |
|    0 |    0 |    0 |    1 |       1 | The Gregorian time-based UUID specified in this document.                     |
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
{: #table2 title='UUID variant 10x versions defined by this specification'}

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

## UUID Version 1 {#uuidv1}
UUID Version 1 is a time-based UUID featuring a 60-bit timestamp
represented by Coordinated Universal Time (UTC) as a count of 100-
nanosecond intervals since 00:00:00.00, 15 October 1582 (the date of
Gregorian reform to the Christian calendar).

UUID Version 1 also features a clock sequence field which is used to help avoid
duplicates that could arise when the clock is set backwards in time
or if the node ID changes.

The node field consists of an IEEE 802 MAC
address, usually the host address.  For systems with multiple IEEE
802 addresses, any available one MAY be used.  The lowest addressed
octet (octet number 10) contains the global/local bit and the
unicast/multicast bit, and is the first octet of the address
transmitted on an 802.3 LAN.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           time_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|           time_mid            |  ver  |       time_high       |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|         clock_seq         |             node              |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                              node                             |
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

ver:
: The 4 bit version field as defined by {{version_field}} set to 0001.
  Occupies bits 48 through 51 of octet 6.

time_high:
: 12 bits that will contain the most significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 52 through 63 (octets 6-7)

var:
: The 2 bit variant field as defined by {{variant_field}} set to 10.
  Occupies bits 64 and 65 of octet 8.

clock_seq:
:  The 14-bits containing the clock sequence.
  Occupies bits 66 through 79 (octets 8-9).

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
the value to which the clock was set, then the clock sequence MUST
be changed.  If the previous value of the clock sequence is known, it
MAY be incremented; otherwise it SHOULD be set to a random or
high-quality pseudo-random value.

Similarly, if the node ID changes (e.g., because a network card has
been moved between machines), setting the clock sequence to a random
number minimizes the probability of a duplicate due to slight
differences in the clock settings of the machines.  If the value of
clock sequence associated with the changed node ID were known, then
the clock sequence MAY be incremented, but that is unlikely.

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
This MD5 value is then used to populate all 128 bits of the UUID layout.
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
: The 4 bit version field as defined by {{version_field}} set to 0011

md5_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following md5_high
  from the computed MD5 value.

var:
: The 2 bit variant field as defined by {{variant_field}} set to 10

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
: The first 48 bits of the layout that can be filled with random data as specified in {{unguessability}}

ver:
: The 4 bit version field as defined by {{version_field}} set to 0100

random_b:
: 12 more bits of the layout that can be filled random data as per {{unguessability}}

var:
: The 2 bit variant field as defined by {{variant_field}} set to 10

random_c:
: The final 62 bits of the layout immediately following the var field to be
  filled with random data as per {{unguessability}}

## UUID Version 5 {#uuidv5}
UUID Version 5 is meant for generating UUIDs from "names"
that are drawn from, and unique within, some "name space" as per {{name_based_uuid_generation}}.

UUIDv5 values are created by computing an SHA1 {{SHA1}}
hash over a given name space value concatenated with the desired name value
after both have been converted to a canonical sequence of octets in network byte order.
This SHA1 value is then used to populate all 128 bits of the UUID layout. Excess bits beyond 128 are discarded.
The UUID version and variant then replace the respective bits as defined by {{version_field}} and {{variant_field}}

Some common name space values have been defined via {{namespaces}}.

There may be scenarios, usually depending on organizational security policies, where SHA1 libraries may not be available or deemed unsafe for use.
As such it may be desirable to generate name-based UUIDs derived from SHA256 or newer SHA methods. These name-based UUIDs MUST NOT utilize UUIDv5 and MUST be within the UUIDv8 space defined by {{v8}}.
For implementation guidance around utilizing UUIDv8 for name-based UUIDs refer to the sub-section of {{name_based_uuid_generation}}.

For more information on SHA1 security considerations see {{RFC6194}}.

~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           sha1_high                           |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|         sha1_high             |  ver  |      sha1_mid         |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|                       sha1_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           sha1_low                            |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
~~~~
{: title='UUIDv5 Field and Bit Layout'}

{: vspace='0'}

sha1_high:
: The first 48 bits of the layout are filled
  with the most significant, left-most 48 bits
  from the computed SHA1 value.

ver:
: The 4 bit version field as defined by {{version_field}}

sha1_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following sha1_high
  from the computed SHA1 value.

var:
: The 2 bit variant field as defined by {{variant_field}}.

sha1_low:
: The final 62 bits of the layout immediately following the var field to be
  filled by skipping the 2 most significant, left-most bits of the remaining SHA1 hash
  and then using the next 62 most significant, left-most bits.
  Any leftover SHA1 bits are discarded and unused.

## UUID Version 6 {#uuidv6}

UUID version 6 is a field-compatible version of UUIDv1, reordered for improved
DB locality.
It is expected that UUIDv6 will primarily be used in contexts where there
are existing v1 UUIDs.
Systems that do not involve legacy UUIDv1 SHOULD use UUIDv7 instead.

Instead of splitting the timestamp into the low, mid and high sections from
UUIDv1, UUIDv6 changes this sequence so timestamp bytes are stored from most
to least significant.
That is, given a 60 bit timestamp value as specified for UUIDv1 in {{uuidv1}},
for UUIDv6, the first 48 most significant bits are stored
first, followed by the 4 bit version (same position), followed by the remaining
12 bits of the original 60 bit timestamp.

The clock sequence bits remain unchanged from their usage and position in {{uuidv1}}.

The clock sequence and node bits SHOULD be reset to a pseudo-random value for each new UUIDv6 generated; however, implementations MAY choose to retain the old MAC address behavior from {{uuidv1}}. For more information on MAC address usage within UUIDs see the {{Security}}.

The format for the 16-byte, 128 bit UUIDv6 is shown in {{v6layout}}


~~~~
 0                   1                   2                   3
 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                           time_high                           |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|           time_mid            |  ver  |       time_low        |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|var|         clock_seq         |             node              |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                              node                             |
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

ver:
: The 4 bit version field as defined by {{version_field}} set to 0110.
  Occupies bits 48 through 51 of Octet 6.

time_low:
: 12 bits that will contain the least significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 52 through 63 (octets 6-7)

var:
: The 2 bit variant field as defined by {{variant_field}} set to 10.
  Occupies bits 64 and 65 of octet 8.

clock_seq:
: The 14 bits containing the clock sequence.
  Occupies bits 66 through 79 (octets 8-9).

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
UUID verion 7 also has improved entropy characteristics over versions 1 or 6.

Implementations SHOULD utilize UUID version 7 instead of UUID version 1 and 6 if
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
: 48 bit big-endian unsigned number of Unix epoch timestamp in milliseconds as per {{timestamp_considerations}}.

ver:
: 4 bit UUIDv7 version set as per {{version_field}}

rand_a:
: 12 bits pseudo-random data to provide uniqueness as per {{unguessability}} and/or an optional counter to guarantee additional monotonicity as per {{monotonicity_counters}}.

var:
: The 2 bit variant defined by {{variant_field}}.

rand_b:
: The final 62 bits of pseudo-random data to provide uniqueness as per {{unguessability}} and/or an optional counter to guarantee additional monotonicity as per {{monotonicity_counters}}.


## UUID Version 8 {#v8}

UUID version 8 provides an RFC-compatible format for experimental or vendor-specific
use cases.
The only requirement is that the variant and version bits MUST be set as
defined in {{variant_field}} and {{version_field}}.
UUIDv8's uniqueness will be implementation-specific and MUST NOT be assumed.

The only explicitly defined bits are the Version and Variant leaving 122
bits
for implementation specific UUIDs. To be clear:
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
implementation. Various relevant factors are covered
below to help guide an implementer through the different trade-offs among
differing UUID implementations.

## Timestamp Considerations {#timestamp_considerations}

UUID timestamp source, precision and length was the topic of great debate
while creating UUIDv7 for this specification. Choosing the right timestamp for
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
  epoch are required UUIDv8 SHOULD be used.

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
  Care SHOULD be given to ensure that the proper length is selected for a given
  timestamp.
  UUID version 1 and 6 utilize a 60 bit timestamp valid until 5623 AD and UUIDv7 features a 48
  bit timestamp valid until the year 10889 AD.

Altering, Fuzzing, or Smearing:
: Implementations MAY alter the actual timestamp. Some examples include security
  considerations around providing a real clock value within a UUID, to correct
  inaccurate clocks, or to handle leap seconds. This specification makes no
  requirement or guarantee about how close the clock value needs to be to the actual
  time.
  If UUIDs do not need to be frequently generated, the UUIDv1 or UUIDv6 timestamp can
  simply be the system time multiplied by the number of 100-nanosecond
  intervals per system time interval.

Padding:
: When timestamp padding is required, implementations MUST pad the most significant
  bits (left-most) bits with zeros. An example is padding the most significant,
  left-most bits of a 32 bit Unix timestamp with zeros to fill out the 48
  bit timestamp in UUIDv7.

Truncating:
: When timestamps need to be truncated, the lower, least significant
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
  Similar techniques are discussed in {{distributed_shared_knowledge}}.

## Monotonicity and Counters {#monotonicity_counters}

Monotonicity is the backbone of time-based sortable UUIDs. Normally, time-based
UUIDs from this document will be monotonic due to an embedded timestamp; however,
implementations can guarantee additional monotonicity via the concepts covered
in this section.

Care SHOULD be taken to ensure UUIDs generated in batches are
also monotonic. That is, if one thousand UUIDs are generated for the same
timestamp, there SHOULD be sufficient logic for organizing the creation order of
those one thousand UUIDs.
Batch UUID creation implementations MAY utilize a monotonic counter that
SHOULD increment for each UUID created during a given timestamp.

For single-node UUID implementations that do not need to create batches of
UUIDs, the embedded timestamp within UUID version 6 and 7 can provide
sufficient monotonicity guarantees by simply ensuring that timestamp increments
before creating a new UUID. Distributed nodes are discussed in
{{distributed_shared_knowledge}}.

Implementations SHOULD choose one method for single-node UUID implementations
that require batch UUID creation, or are otherwise concerned about monotonicity
with high frequency UUID generation.

{: vspace='0'}

Fixed-Length Dedicated Counter Bits (Method 1):
: Some implementations allocate a specific number of bits in the
  UUID layout to the sole purpose of tallying the total number of UUIDs created
  during a given UUID timestamp tick.
  A fixed bit-length counter, if present, SHOULD be positioned immediately after the
  embedded timestamp. This promotes sortability and allows random data generation
  for each counter increment.
  With this method, the rand_a section of UUIDv7 SHOULD be used as fixed-length
  dedicated counter bits that are incremented by one for every UUID generation.
  The trailing random bits generated for each new UUID in rand_b can help produce
  unguessable UUIDs. In the event more counter bits are required, the most significant
  (left-most) bits of rand_b MAY be used as additional counter bits.

Monotonic Random (Method 2):
: With this method, the random data is extended to also function as a counter.
  This monotonic value can be thought of as a "randomly seeded counter" which
  MUST be incremented in the least significant position for each UUID created
  on a given timestamp tick.
  UUIDv7's rand_b section SHOULD be utilized with this method to handle batch
  UUID generation during a single timestamp tick.
  The increment value for every UUID generation SHOULD be a random integer
  of any desired length larger than zero. It ensures the UUIDs retain the required
  level of unguessability provided by the underlying entropy.
  The increment value MAY be one when the number of UUIDs generated in a particular
  period of time is important and guessability is not an issue. However, it
  SHOULD NOT be used by implementations that favor unguessiblity, as the resulting
  values are easily guessable.

Re-randomize Until Monotonic (Method 3):
: If the performance impact is acceptable (depending on the UUID version,
  granularity of the system clock, and expected throughput of values
  generated per clock value), an implementation can, in the case
  of multiple UUID values using the same clock tick, simply regenerate
  a new random value as many times as needed in order to produce a UUID that is
  ordered after the last one.  The primary benefit of this approach is simplicity
  of implementation. One downside to this approach is the fact that
  generation will become increasingly slower for a given timestamp value as
  more attempts are required to produce monotonic output, and the fact that
  subsequent values will have less entropy and be more easily guessable.

Replace Left-Most Random Bits with Increased Clock Precision (Method 4):
: For UUIDv7, which has millisecond timestamp precision, it is possible
  to use any additional clock precision available on the system to substitute
  for random bits immediately following the timestamp.  This can provide
  values that are time-ordered with sub-millisecond precision, using
  however many bits are appropriate in the implementation environment.
  With this method, the additional time precision bits MUST follow the
  timestamp as the next available bit, in the rand_a field for UUIDv7.

  To calculate this value, start with the portion of the timestamp
  expressed as a fraction of clock's tick value (fraction of a millisecond
  for UUIDv7).  Compute the maximum value that can be represented in
  the available bit space, 4095 for the UUIDv7 rand_a field.
  Using floating point math, multiply this fraction of a millisecond
  value by 4095 and round to an integer result to arrive at a number
  between 0 and the maximum allowed for the indicated bits
  which is sorts monotonically based on time. Each increasing fractional
  value will result in an increasing bit field value, to the
  precision available with these bits.
  
  For example, let's assume a system timestamp of 1 Jan 2023 12:34:56.1234567.
  Taking the precision greater than 1ms gives us a value of 0.4567, as a
  fraction of a millisecond.  If we wish to encode this as 12 bits, we can
  take the maximum value that fits in those bits (4095, or 2 to the 12th power minus 1)
  and multiply it by our millisecond fraction value of 0.4567 and round the result to
  an integer, which gives an integer value of 1870. Expressed as hex it is
  0x74E, or the binary bits 011101001110.  One can then use those 12 bits
  as the most significant (left-most) portion of the random section of the UUID
  (e.g. the rand_a field in UUIDv7).
  This works for any desired bit length that fits into a UUID and applications
  can decide the appropriate length based on available clock precision and desired
  random bits.

  The main benefit to encoding additional timestamp precision
  is that it utilizes additional time precision already available in the system clock
  to provide values that are more likely to be unique, and thus may simplify
  certain implementations. This technique can also be used in conjunction with one
  of the other methods, where this additional time precision would immediately
  follow the timestamp and then if any bits are to be used as clock sequence
  they would follow next.

The following sub-topics cover topics related solely with creating reliable
fixed-length dedicated counters:

{: vspace='0'}

Fixed-Length Dedicated Counter Seeding:
: Implementations utilizing the fixed-length counter method SHOULD randomly initialize
  the counter with each new timestamp tick.
  However, when the timestamp has not incremented, the counter SHOULD be frozen
  and incremented via the desired increment logic.
  When utilizing a randomly seeded counter alongside Method 1, the random value MAY
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
  For example, millisecond precision generally requires a larger counter than a
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
: The technique from Fixed-Length Dedicated Counter Seeding that describes
  allocating a segment of the fixed-length counter as a rollover guard is also
  helpful to mitigate counter rollover issues.
  This same technique can be used with monotonic random counter methods
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



1. If the current timestamp is equal to the previous timestamp, increment the
  counter according to the desired method.



1. If the current timestamp is greater than the previous timestamp, re-initialize
  the desired counter method to the new timestamp and generate new random bytes
  (if the bytes were frozen or being used as the seed for a monotonic counter).

{: vspace='0'}

Monotonic Error Checking:
: Implementations SHOULD check if the the currently generated UUID is greater
than the previously generated UUID. If this is not the case then any number
of things could have occurred, such as clock rollbacks,
leap second handling, and counter rollovers. Applications SHOULD embed sufficient
logic to catch these scenarios and correct the problem to ensure that the next
UUID generated is greater than the previous. To handle this scenario, the
general guidance is that application MAY reuse the previous timestamp and
increment the previous counter method.

## UUID Generator States {#generator_states}

The UUID generator state only needs to be read from stable storage once at boot
time, if it is read into a system-wide shared volatile store (and
updated whenever the stable store is updated).

This stable storage MAY be used to record various portions of the UUID generation
which prove useful for batch UUID generation purposes and monotonic error checking with UUIDv6 and UUIDv7.
These stored values include but are not limited to last known timestamp, clock sequence, counters and random data.

If an implementation does not have any stable store available, then
it SHOULD proceed with UUID generation as if this was the first UUID created within a batch.
This is the least desirable implementation because it will increase the frequency
of creation of values such as clock sequence, counters or random data which increases the
probability of duplicates.

An implementation MAY also return an application error in the event that collision resistance is of the utmost concern.
The semantics of this error are up to the application and implementation.
See {{collision_resistance}} for more information on weighting collision tolerance in applications.

For UUIDv1 and UUIDv6, if the node ID can never change (e.g., the network interface card
from which the node ID is derived is inseparable
from the system), or if any change also re-initializes the clock
sequence to a random value, then instead of keeping it in stable
store, the current node ID may be returned.

For UUIDv1 and UUIDv6, the state does not always need to be written to stable store every
time a UUID is generated.  The timestamp in the stable store can be
periodically set to a value larger than any yet used in a UUID.  As
long as the generated UUIDs have timestamps less than that value, and
the clock sequence and node ID remain unchanged, only the shared
volatile copy of the state needs to be updated.  Furthermore, if the
timestamp value in stable store is in the future by less than the
typical time it takes the system to reboot, a crash will not cause a
re-initialization of the clock sequence.

If it is too expensive to access shared state each time a UUID is
generated, then the system-wide generator can be implemented to
allocate a block of time stamps each time it is called; a per-
process generator can allocate from that block until it is exhausted.

## Distributed UUID Generation {#distributed_shared_knowledge}

Some implementations MAY desire to utilize multi-node, clustered, applications
which involve two or more
nodes independently generating UUIDs that will be stored in a common location.
While UUIDs already feature sufficient entropy to ensure that the chances
of collision are low, as the total number of UUID generating nodes increase; so does the likelihood
of a collision.

This section will detail the two additional collision resistance approaches that have been observed by by multi-node
UUID implementations in distributed environments.

It should be noted that although this section details two methods for the sake of completeness;
implementations SHOULD utilize the pseudo-random Node ID option if additional collision resistance for distributed UUID generation is a requirement.
Likewise, utilization of either method is not required for implementing UUID generation in distributed environments.

{: vspace='0'}

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

Centralized Registry:
: With this method all nodes tasked with creating UUIDs consult a central registry
  and confirm the generated value is unique. As applications scale, the communication
  with the central registry could become a bottleneck and impact UUID generation
  in a negative way. Shared knowledge schemes with central/global
  registries are outside the scope of this specification and is NOT RECOMMENDED.

Distributed applications generating UUIDs at a variety of hosts MUST
be willing to rely on the random number source at all hosts.  If this
is not feasible, the namespace variant should be used.

## Name-Based UUID Generation {#name_based_uuid_generation}
The concept of name and name space should be broadly construed, and not
limited to textual names.  For example, some name spaces are the
domain name system, URLs, Object Identifiers (OIDs), X.500 Distinguished
Names (DNs), and reserved words in a programming language.  The
mechanisms or conventions used for allocating names and ensuring
their uniqueness within their name spaces are beyond the scope of
this specification.

The requirements for name-based UUIDs are as follows:

* UUIDs generated at different times from the same name in the
  same namespace MUST be equal.

* UUIDs generated from two different names in the same namespace
  should be different (with very high probability).

* UUIDs generated from the same name in two different namespaces
  should be different (with very high probability).

* If two UUIDs that were generated from names are equal, then they
  were generated from the same name in the same namespace (with very
  high probability).

{: vspace='0'}

A note on namespaces:
: While {{namespaces}} details a few interesting namespaces; implementations SHOULD provide the ability input a custom namespace.
  For example, any other UUID MAY be generated and uses as the desired namespace input for a given application context to
  ensure all names created are unique within the newly created namespace.

Name-based UUIDs using version 8:
: As per {{uuidv5}} name-based UUIDs that desire to use modern hashing algorithms MUST be created within the UUIDv8 space.
 These MAY leverage newer hashing protocols such as SHA256, SHA512, {{SHA3}} or even protocols that have not been defined yet.
 To ensure UUIDv8 Name-Based UUID values of different hashing protocols can exist in the same bit space; this document defines various "hashspaces" in {{hashspaces}}.
 Creation of name-based version 8 UUIDs follow the same logic defined in {{uuidv5}} but the hashspace should be used to as the starting point with the desired
 namespace and name concatenated to the end of the hashspace.
 Then an implementation may apply the desired hashing algorithm to the entire value after all have been converted to a canonical sequence of octets in network byte order.
 Ensure the version and variant and variant bits are modified as per {{v8}} bit layout and finally trim any excess bits beyond 128.
 An important note for secure hashing algorithms that produce variable rate outputs, such as those found in SHAKE, the output hash MUST be 128 bits or larger.
 See {{uuidv8_example_name}} for a SHA256 UUIDv8 example test vector.

Advertising the Hash Algorithm:
: Name-based UUIDs utilizing UUIDv8 do not allocate any available bits to identifying the hashing algorithm.
  As such where common knowledge about the hashing algorithm for a given UUIDv8 name-space UUID is required, sharing the Hash Space ID proves useful for identifying a the algorithm.
  That is, to detail SHA2-256 was used to create a given UUIDv8 name-based UUID an implementation may also share the "3fb32780-953c-4464-9cfd-e85dbbe9843d" hash space which uniquely identifies the SHA2-256 hashing algorithm for the purpose of UUIDv8. Mind you that this need not be the only method of sharing the hashing algorithm; this is one example of how two systems could share knowledge.
  The protocol of choice, communication channels and actual method of sharing this data between systems it outside the scope of this specification.

## Collision Resistance {#collision_resistance}

Implementations SHOULD weigh the consequences of UUID collisions within their
application and when deciding between UUID versions that use entropy (randomness)
versus the other components such as those in {{timestamp_considerations}} and {{monotonicity_counters}}.
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
knowledge scheme, a shared knowledge scheme is not required by UUID to provide
uniqueness guarantees.
Implementations MAY implement a shared knowledge scheme introduced in {{distributed_shared_knowledge}} as they see fit to extend the uniqueness guaranteed this specification.


## Unguessability {#unguessability}
Implementations SHOULD utilize a cryptographically secure pseudo-random number
generator (CSPRNG) to provide values that are both difficult to predict ("unguessable")
and have a low likelihood of collision ("unique").
Care SHOULD be taken to ensure the CSPRNG state is properly reseeded upon
state changes, such as process forks, to ensure proper CSPRNG operation.
CSPRNG ensures the best of {{collision_resistance}} and {{Security}} are present in modern UUIDs.

Further advice on generating cryptographic-quality random numbers can be found in {{RFC4086}} and in {{RANDOM}}.

## UUIDs that Do Not Identify the Host {#unidentifiable}
This section describes how to generate a UUIDv1 or UUIDv6 value if an IEEE
802 address is not available, or its use is not desired.

Implementations SHOULD obtain a 47-bit cryptographic-quality random
number as per {{unguessability}} and use it as the low 47 bits of the node ID.

Implementations MUST set the least significant bit of the first octet of the node ID set to one to create a 48-bit node id.
This bit is the unicast/multicast bit, which will never be set in IEEE 802
addresses obtained from network cards.  Hence, there can never be a
conflict between UUIDs generated by machines with and without network
cards.

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

UUIDs formats created by this specification SHOULD be lexicographically sortable
while in the textual representation.

UUIDs created by this specification are crafted with big-endian byte order
(network byte order) in mind. If little-endian style is required a custom
UUID format SHOULD be created using UUIDv8.


## Opacity {#opacity}

UUIDs SHOULD be treated as opaque values and implementations SHOULD NOT examine
the bits in a UUID. However,
inspectors MAY refer to {{variant_field}} and {{version_field}} when required to determine UUID version and variant.


## DBMS and Database Considerations {#database_considerations}

For many applications, such as databases, storing UUIDs as text is unnecessarily
verbose, requiring 288 bits to represent 128 bit UUID values.
Thus, where feasible, UUIDs SHOULD be stored within database applications
as the underlying 128 bit binary value.

For other systems, UUIDs MAY be stored in binary form or as text, as appropriate.
The trade-offs to both approaches are:


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
There is no update required to the IANA URN namespace registration {{URNNamespaces}} for UUID filed in {{RFC4122}}.
Further, at this time the authors and working group have concluded that IANA is not required to track UUIDs used for identifying items such as versions, variants, namespaces or hashspaces.

# Community Considerations {#community}

The use of UUIDs is extremely pervasive in computing.  They comprise
the core identifier infrastructure for many operating systems
such as Microsoft Windows and applications such as the Mozilla Web browser and in
many cases, become exposed in many non-standard ways.

This specification attempts to standardize that practice as openly as
possible and in a way that attempts to benefit the entire Internet.

# Security Considerations {#Security}

Implementations MUST NOT assume that UUIDs are hard to guess.
Foe example, they MUST not be used
as security capabilities (identifiers whose mere possession grants
access).  Discovery of predictablity in a random number source will
result in a vulnerability.

Implementations MUST NOT assume that it is easy to determine if a UUID has been
slightly transposed in order to redirect a reference to another
object.  Humans do not have the ability to easily check the integrity
of a UUID by simply glancing at it.

MAC addresses pose inherent security risks and SHOULD not be used within
a UUID.
Instead CSPRNG data SHOULD be selected from a source with sufficient entropy
to ensure guaranteed
uniqueness among UUID generation. See {{unguessability}} and {{unidentifiable}} for more information.

Timestamps embedded in the UUID do pose a very small attack surface. The
timestamp in conjunction with
an embedded counter does signal the order of creation for a given UUID and
its corresponding data but
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
Sergey Prokhorenko,
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

# Some Name Space IDs {#namespaces}

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

# Some Hash Space IDs {#hashspaces}
This appendix lists the hash space IDs for use with UUIDv8 name-based UUIDs.

~~~~
SHA2_224     = "59031ca3-fbdb-47fb-9f6c-0f30e2e83145"
SHA2_256     = "3fb32780-953c-4464-9cfd-e85dbbe9843d"
SHA2_384     = "e6800581-f333-484b-8778-601ff2b58da8"
SHA2_512     = "0fde22f2-e7ba-4fd1-9753-9c2ea88fa3f9"
SHA2_512_224 = "003c2038-c4fe-4b95-a672-0c26c1b79542"
SHA2_512_256 = "9475ad00-3769-4c07-9642-5e7383732306"
SHA3_224     = "9768761f-ac5a-419e-a180-7ca239e8025a"
SHA3_256     = "2034d66b-4047-4553-8f80-70e593176877"
SHA3_384     = "872fb339-2636-4bdd-bda6-b6dc2a82b1b3"
SHA3_512     = "a4920a5d-a8a6-426c-8d14-a6cafbe64c7b"
SHAKE_128    = "7ea218f6-629a-425f-9f88-7439d63296bb"
SHAKE_256    = "2e7fc6a4-2919-4edc-b0ba-7d7062ce4f0a"
~~~~


# Test Vectors {#test_vectors}

Both UUIDv1 and UUIDv6 test vectors utilize the same 60 bit timestamp: 0x1EC9414C232AB00
(138648505420000000) Tuesday, February 22, 2022 2:22:22.000000 PM GMT-05:00

Both UUIDv1 and UUIDv6 utilize the same values in clock_seq,
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

## Example of a UUIDv1 Value {#uuidv1_example}
~~~~
----------------------------------------------
field                 bits    value
----------------------------------------------
time_low              32      0xC232AB00
time_mid              16      0x9414
ver                    4      0x1
time_high             12      0x1EC
var                    2      b10
clock_seq             14      b11, 0x3C8
node                  48      0x9E6BDECED846
----------------------------------------------
total                128
----------------------------------------------
final_hex: C232AB00-9414-11EC-B3C8-9E6BDECED846
~~~~
{: title='UUIDv1 Example Test Vector'}

## Example of a UUIDv3 Value {#uuidv3_example}
The MD5 computation from is detailed in {{v3md5}} using the DNS NameSpace and the Name "www.example.com".
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

## Example of a UUIDv4 Value {#uuidv4_example}
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


## Example of a UUIDv5 Value {#uuidv5_example}
The SHA1 computation from is detailed in {{v5sha1}} using the DNS NameSpace and the Name "www.example.com".
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
sha1_high  48      0x2ed6657de927
ver         4      0x5
sha1_mid   12      0x68b
var         2      b10
sha1_low   62      b01, 0x5e12665a8aea6a2
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
ver                     4     0x6
time_high              12     0xB00
var                     2     b10
clock_seq              14     b11, 0x3C8
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


## Example of a UUIDv8 Value (time-based) {#uuidv8_example}

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
{: title='UUIDv8 Example Time-based Test Vector'}

## Example of a UUIDv8 Value (name-based) {#uuidv8_example_name}
A SHA256 version of {{uuidv5_example}} is detailed in {{v8sha256}} to detail the usage of hash spaces alongside namespace and names.
The field mapping and all values are illustrated in {{v8fieldssha256}}.
Finally to further illustrate the bit swapping for version and variant and the unused/discarded part of the SHA256 value see {{v8vervar}}.

~~~~
Hash Space (SHA2_256):  3fb32780-953c-4464-9cfd-e85dbbe9843d
Name Space (DNS):       6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:                   www.example.com
-----------------------------------------------
SHA256:                 401835fda627a70a073fed73f2bc5b2c2a8936385a38a9c133de0ca4af0dfaed
~~~~
{: id='v8sha256' title='UUIDv8 Example SHA256'}

~~~~
-------------------------------
field      bits    value
-------------------------------
custom_a     48    0x401835fda627
ver           4    0x8
custom_b     12    0x627
var           2    b10
custom_c     62    b0, 0x73fed73f2bc5b2c
-------------------------------
total       128
-------------------------------
final: 401835fd-a627-870a-873f-ed73f2bc5b2c
~~~~
{: id='v8fieldssha256' title='UUIDv8 Example Name-Based SHA256 Test Vector'}

~~~~
SHA256 hex and dash:      401835fd-a627-a70a-073f-ed73f2bc5b2c-2a8936385a38a9c133de0ca4af0dfaed
Ver and Var Overwrite:    xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                    401835fd-a627-870a-873f-ed73f2bc5b2c
Discarded:                                                    -2a8936385a38a9c133de0ca4af0dfaed
~~~~
{: id='v8vervar' title='UUIDv8 Example Ver/Var bit swaps and discarded SHA256 segment'}
