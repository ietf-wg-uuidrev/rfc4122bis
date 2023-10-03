---
v: 3
docname: draft-ietf-uuidrev-rfc4122bis-12
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
title: Universally Unique IDentifiers (UUID)
abbrev: UUID
area: ART
wg: uuidrev
kw: uuid
date: 2023

author:
- name: Kyzer R. Davis
  email: kydavis@cisco.com
  org: Cisco Systems
- name: Brad G. Peabody
  email: brad@peabody.io
  org: Uncloud
- ins: P. Leach
  name: P. Leach
  email: pjl7@uw.edu
  org: University of Washington

normative:
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
  RFC4086: RFC4086
  RFC8141: RFC8141
  RFC8937: RFC8937
  FIPS180-4:
    target: https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf
    title: Secure Hash Standard
    author:
    - org: National Institute of Standards and Technology
    date: August 2015
    seriesinfo:
      FIPS: PUB 180-4
  FIPS202:
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

informative:
  RFC1321: RFC1321
  RFC1738: RFC1738
  RFC4122: RFC4122
  RFC5234: RFC5234
  RFC6151: RFC6151
  RFC6194: RFC6194
  RFC7042: RFC7042
  RFC8126: RFC8126
  RFC8499: RFC8499
  X500:
    seriesinfo:
      ISO/IEC: '9594-1'
      ITU-T Rec.: X.500
    title: >
      Information technology – Open Systems Interconnection – The Directory: Overview of concepts, models and services
    date: 2019
  X660:
    seriesinfo:
      ISO/IEC: '9834-1'
      ITU-T Rec.: X.660
    title: >
      Information technology – Procedures for the operation of object identifier registration authorities: General procedures and top arcs of the international object identifier tree
    date: 2011
  X680:
    seriesinfo:
      ISO/IEC: '8824-1:2021'
      ITU-T Rec.: X.680
    title: >
      Information Technology - Abstract Syntax Notation One (ASN.1) & ASN.1 encoding rules
    date: 2021
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
  Python:
    target: https://docs.python.org/3/library/uuid.html
    title: UUID objects according to RFC
    author:
    - org: Python
    date: 2023-05-23
  Microsoft:
    target: https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-dtyp/a66edeb1-52a0-4d64-a93b-2f5c833d7d92
    title: curly braced GUID string
    author:
    - org: Microsoft
    date: 2023-04-03
  MS_COM_GUID:
    target: https://devblogs.microsoft.com/oldnewthing/20220928-00/?p=107221
    title: Why does COM express GUIDs in a mix of big-endian and little-endian? Why can’t it just pick a side and stick with it?
    author:
    - name: Raymond Chen
    date: 2022-09-28
  IBM_NCS:
    target: https://www.ibm.com/docs/en/aix/7.1?topic=u-uuid-gen-command-ncs
    title: uuid_gen Command (NCS)
    author:
    - org: IBM
    date: 2023-03-23
  RANDOM:
    target: https://peteroupc.github.io/random.html
    title: "Random Number Generator Recommendations for Applications"
    author:
    - name: Peter Occil
    date: 2023

--- abstract

This specification defines the UUIDs (Universally Unique IDentifiers) and the UUID Uniform Resource Name (URN) namespace. UUIDs are also known as GUIDs (Globally Unique IDentifiers).
A UUID is 128 bits long and is intended to guarantee
uniqueness across space and time.  UUIDs were originally used in the
Apollo Network Computing System and later in the Open Software
Foundation's (OSF) Distributed Computing Environment (DCE), and then
in Microsoft Windows platforms.

This specification is derived from the DCE specification with the
kind permission of the OSF (now known as The Open Group).
Information from earlier versions of the DCE specification have been
incorporated into this document. This document obsoletes RFC4122.

--- middle

# Introduction {#Background}

This specification defines the UUIDs (Universally Unique IDentifiers) and the UUID Uniform Resource Name (URN) namespace. UUIDs are also known as GUIDs (Globally Unique IDentifiers).
A UUID is 128 bits long and requires no central
registration process.

The use of UUIDs is extremely pervasive in computing.  They comprise
the core identifier infrastructure for many operating systems
such as Microsoft Windows and applications such as the Mozilla Web browser and in
many cases, become exposed in many non-standard ways.

This specification attempts to standardize that practice as openly as
possible and in a way that attempts to benefit the entire Internet.
The information here is meant to be a concise guide for those wishing
to implement services using UUIDs either in combination with URNs {{RFC8141}} or otherwise.

There is an ITU-T Recommendation and an ISO/IEC Standard {{X667}} that are
derived from {{RFC4122}}.  Both sets of
specifications have been aligned and are fully technically
compatible.
Nothing in this document should be construed to override the DCE standards that defined UUIDs.

# Motivation {#motivation}

One of the main reasons for using UUIDs is that no centralized
authority is required to administer them (although two formats may leverage optional
IEEE 802 node identifiers, others do not).  As a result, generation
on demand can be completely automated and used for a variety of
purposes.  The UUID generation algorithm described here supports very
high allocation rates of 10 million per second per machine or more if
necessary, so that they could even be used as transaction IDs.

UUIDs are of a fixed size (128 bits), which is reasonably small
compared to other alternatives.  This lends itself well to sorting,
ordering, and hashing of all sorts, storing in databases, simple
allocation, and ease of programming in general.

Since UUIDs are unique and persistent, they make excellent Uniform
Resource Names.  The unique ability to generate a new UUID without a
registration process allows for UUIDs to be one of the URNs with the
lowest minting cost.

## Update Motivation

Many things have changed in the time since UUIDs were originally created.
Modern applications have a need to create and utilize UUIDs as the primary
identifier for a variety of different items in complex computational systems,
including but not limited to database keys, file names, machine or system
names, and identifiers for event-driven transactions.

One area in which UUIDs have gained popularity is database keys.
This stems from the increasingly distributed nature of modern applications.
In such cases, "auto increment" schemes often used by databases do not work
well, as the effort required to coordinate sequential numeric identifiers across
a network can easily become a burden.
The fact that UUIDs can be used to create unique, reasonably short values
in distributed systems without requiring coordination makes them a good
alternative, but UUID versions 1-5, which were originally defined by {{RFC4122}}, lack certain other desirable characteristics:


1. Non-time-ordered UUID versions such as UUIDv4 (described in {{uuidv4}}) have poor database index
  locality.
  This means that new values created in succession are not close to each other in
  the index and thus require inserts to be performed at random
  locations.
  The resulting negative performance effects on common structures used for
  this (B-tree and its variants) can be dramatic.

1. The 100-nanosecond Gregorian epoch used in UUIDv1 (described in {{uuidv1}}) timestamps is uncommon
  and difficult to represent accurately using a standard number format such
  as {{IEEE754}}.

1. Introspection/parsing is required to order by time sequence, as opposed to
  being able to perform a simple byte-by-byte comparison.

1. Privacy and network security issues arise from using a MAC address in the
  node field of UUID version 1.
  Exposed MAC addresses can be used as an attack surface to locate network interfaces
  and reveal various other
  information about such machines (minimally manufacturer, potentially other
  details). Additionally, with the advent of virtual machines and containers,
  MAC address uniqueness is no longer guaranteed.

1. Many of the implementation details specified in {{RFC4122}} involved trade
  offs that are neither possible to specify for all applications nor
  necessary to produce interoperable implementations.

1. {{RFC4122}} did not distinguish between the requirements for generating a UUID
   and those for simply storing one, although they are often different.

Due to the aforementioned issues, many widely distributed database applications
and large application vendors have sought to solve the problem of creating
a better
time-based, sortable unique identifier for use as a database key. This has
led to numerous implementations
over the past 10+ years solving the same problem in slightly different ways.

While preparing this specification, the following 16 different implementations
were analyzed for trends in total ID length, bit layout, lexical formatting/encoding,
timestamp type, timestamp format, timestamp accuracy, node format/components,
collision handling, and multi-timestamp tick generation sequencing:


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
led to this document which intends to adapt new UUIDs to address these issues.

Further, {{RFC4122}} itself was in need an overhaul to address a number of topics such as but not limited to the following:

1. Miscellaneous erratas. Mostly around bit layout clarifications which lead to inconsistent implementations.

1. Decouple other UUID versions from UUIDv1 bit layout so that fields like "time_hi_and_version" do not need to be referenced within a non-time-based UUID while also providing "UUIDv1 like" definition sections for UUIDv3, UUIDv4, and UUIDv5.

1. Provide implementation best practices around many real-world scenarios and corner cases observed by existing and prototype implementations.

1. Update the document to address security best practices and considerations for the modern age as it pertains MAC addresses, hashing algorithms, secure randomness, and other topics.

1. Provide implementations a standard-based option for implementation specific and/or experimental UUID designs.

1. Provide more test vectors that illustrate real UUIDs created as per the specification.

# Terminology {#terminology}

## Requirements Language {#requirements_language}

{::boilerplate bcp14-tagged}

## Abbreviations {#acronyms}

The following abbreviations are used in this document:

{: indent="14"}
UUID
: Universally Unique Identifier

UUIDv1
: Universally Unique Identifier Version 1

UUIDv2
: Universally Unique Identifier Version 2

UUIDv3
: Universally Unique Identifier Version 3

UUIDv4
: Universally Unique Identifier Version 4

UUIDv5
: Universally Unique Identifier Version 5

UUIDv6
: Universally Unique Identifier Version 6

UUIDv7
: Universally Unique Identifier Version 7

UUIDv8
: Universally Unique Identifier Version 8


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

SHA
: Secure Hash Algorithm

SHA-1
: Secure Hash Algorithm 1 with message digest of 160 bits

SHA-224
: Secure Hash Algorithm with message digest size of 224 bits

SHA-256
: Secure Hash Algorithm with message digest size of 256 bits

SHA-512
: Secure Hash Algorithm with message digest size of 512 bits

SHA-3
: Secure Hash Algorithm 3

SHAKE
: Secure Hash Algorithm 3 based on KECCAK algorithm

UTC
: Coordinated Universal Time

OID
: Object Identifier

## Changelog {#changelog}
{:removeinrfc}

draft-12

{: spacing="compact"}
- Typos #148 #156
- SECDIR Review #141
- SECDIR Review 2 #142
- OPSDIR Review #145
- INDIR Review 2 #140
- IESG Grammar #146
- Revise 16-bit MAC Node Usage #149
- Add MSB3 to Variant Table #153
- Additional Update Motivations #157
- Fix Randomized Node value's mcast bit in Appendix #151
- Request IANA Registry #144
- Describe allocation logic of Namespace ID #161

draft-11

{: spacing="compact"}
- Normalize "name space" to "namespace" everywhere #137
- IANA Review: Verbiage to update RFC4122 references #134
- DNSDIR re-review: Better Define "a canonical sequence of octets" #136
- Crosspost: Typo in Approximate UUID timestamp calculations #135
- INTDIR Review #139

draft-10

{: spacing="compact"}
- ARTART Review and Feedback #130
- Clarify Hash Space IDs listed are not the only options #132
- Add example to timestamp fuzzing #133

draft-09

{: spacing="compact"}
- Late addition of IETF reference for CSPRNG guidance #123
- DNSDIR Review: Typos! #122
- DNSDIR Review: DNS Considerations Update #121
- Error in UUIDv8 Name-based Test Vector #129
- Improve consistency of layout field definitions #128

draft-08

{: spacing="compact"}
- Fix typos #113
- Fix errata 6225 (again) #117 #118
- AD Review: BCP 14 - SHOULD #114
- AD Review: Add proper references to v1 and v6 #116
- AD Review: Remove SHOULD in section 4 #120
- Discuss "front-loaded rollover counter" for 32-bit epoch with Padding method #115

draft-07

{: spacing="compact"}

- Even more grammar tweaks! #109
- Remove unnecessary "32 bit" in UUIDv7 example #108
- Change "fixed millisecond" -> "millisecond by default" relating to v7 #110
- Revert Max UUID Naming #107
- Author Changes

draft-06

{: spacing="compact"}

- More Grammar edits! #102
- Tweak v7 description to de-emphasize optional components #103
- Better Clarify Case in ABNF #104
- Verbiage change in 6.2 #105

draft-05

{: spacing="compact"}

- Changed Max UUID to Max UUID to better complement Latin Nil UUID verbiage. #95
- Align Method 3 text with the 12 bits limitation #96
- Make Version/version casing consistent across 5. UUID Layouts #97
- Cite MS COM GUID as little-endian #95

draft-04

{: spacing="compact"}

- Remove extra words #82, #88, and #93
- Punctuation and minor style fixes #84
- Change rounding mode of Method 4 Section 6.2 #90 (from #86)
- Add verbal description of v7 generation to 5.7. UUID Version 7 #91
- Remove Re-randomize Until Monotonic (Method 3) from Monotonicity and Counters #92
- Fix ambiguous text around UUIDv6 clock sequence #89
- Move endianness statement from layout to format section #85
- Further modified abstract to separate URN topic from UUID definition #83
- Provided three more UUID format examples #83
- Added text further clarifying version construct is for the variant in this doc #83
- Provided further clarification for local/global bit vs multicast bit #83

draft-03

{: spacing="compact"}

- Revised IANA Considerations #71
- Fix "integral numbers of octets" verbiage #67
- Transpose UUID Namespaces to match UUID Hashspaces #70
- Reference all Hash Algorithms. #69
- Normalize SHA abbreviation formats #66
- Add other Hash Abbreviations #65
- Remove URN from title #73
- Move Community Considerations to Introduction #68
- Move some Normative Reference to Informative #74
- Misc formatting changes to address IDNITS feedback
- Downgrade MUST NOT to SHOULD NOT for guessability of UUIDs #75
- Misc. text formatting, typo fixes #78
- Misc. text clarifications #79
- Misc. SHOULD/MUST adjustments #80
- Method 3 and 4 added to monotonic section #81

draft-02

{: spacing="compact"}

- Change md5_high in SHA-1 section to sha1_mid #59
- Describe Nil/Max UUID in variant table #16
- Further Clarify that non-descript node IDs are the preferred method in distributed UUID Generation #49
- Appendix B, consistent naming #55
- Remove duplicate ABNF from IANA considerations #56
- Monotonic Error Checking missing newline #57
- More Security Considerations Randomness #26
- SHA-256 UUID Generation #50
- Expand multiplexed fields within v1 and v6 bit definitions #43
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
- Erroneous reference to v1 in monotonicity #45
- Add Label for "Monotonic Error Checking" paragraph to frame the topic #46
- Remove IEEE paragraph from "uuids that do not identify the host" #48
- Grammar Review #52

draft-00

{: spacing="compact"}
- Merge RFC4122 with draft-peabody-dispatch-new-uuid-format-04.md
- Change: Reference RFC1321 to RFC6151
- Change: Reference RFC2141 to RFC8141
- Change: Reference RFC2234 to RFC5234
- Change: Reference FIPS 180-1 to FIPS 180-4 for SHA-1
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
- Draft 05: MUST verbiage in Reliability of 6.1 #121
- Draft 05: Further discourage centralized registry for distributed UUID Generation.
- New: Further Clarity of exact octet and bit of var/ver in this spec
- New: Block diagram, bit layout, test vectors for UUIDv4
- New: Block diagram, bit layout, test vectors for UUIDv3
- New: Block diagram, bit layout, test vectors for UUIDv5
- New: Add MD5 Security Considerations reference, RFC6151
- New: Add SHA-1 Security Considerations reference, RFC6194

# UUID Format {#format}

The UUID format is 16 octets (128 bits) in size; the variant bits in conjunction with the version
bits described in the next sections determine finer structure. While discussing UUID formats and layout, bit definitions start at 0 and end at 127 while octet definitions start at 0 and end at 15.

In the absence of explicit application or presentation protocol
specification to the contrary, each field is encoded with the Most
Significant Byte first (known as network byte order).

Saving UUIDs to binary format is done by sequencing all fields in big-endian format.
However there is a known caveat that Microsoft's Component Object Model (COM) GUIDs leverage little-endian when saving GUIDs.
The discussion of this {{MS_COM_GUID}} is outside the scope of this specification.

UUIDs MAY be represented as binary data or integers.
When in use with URNs or as text in applications, any given UUID should
be represented by the "hex-and-dash" string format consisting of multiple
groups of upper or lowercase alphanumeric hexadecimal characters separated by single dashes/hyphens.
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

Note that the alphabetic characters may be all uppercase, all lowercase, or mixed case, as per {{RFC5234, Section 2.3}}.
An example UUID using this textual representation from the above ABNF is shown in {{sampleStringUUID}}.

~~~~
f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleStringUUID title='Example String UUID format'}

The same UUID from {{sampleStringUUID}} is represented in Binary ({{sampleBinaryUUID}}), Integer ({{sampleIntegerUUID}}) and as a URN ({{sampleURNUUID}}) defined by {{RFC8141}}.

~~~~
111110000001110101001111101011100111110111101100000100011101000\
01010011101100101000000001010000011001001000111100110101111110110
~~~~
{: #sampleBinaryUUID title='Example Binary UUID'}

~~~~
329800735698586629295641978511506172918
~~~~
{: #sampleIntegerUUID title='Example Integer UUID (shown as a decimal number)'}

~~~~
urn:uuid:f81d4fae-7dec-11d0-a765-00a0c91e6bf6
~~~~
{: #sampleURNUUID title='Example URN UUID'}

There are many other ways to define a UUID format; some examples are detailed below.
Please note that this is not an exhaustive list and is only provided for informational purposes.

{: spacing="compact"}

- Some UUID implementations, such as those found in {{Python}} and {{Microsoft}}, will output UUID with the string format, including dashes, enclosed in curly braces.
- {{X667}} provides UUID format definitions for use of UUID with an OID.
- The legacy {{IBM_NCS}} implementation produces a unique UUID format compatible with Variant 0xx of {{table1}}.

## Variant Field {#variant_field}

The variant field determines the layout of the UUID.  That is, the
interpretation of all other bits in the UUID depends on the setting
of the bits in the variant field.  As such, it could more accurately
be called a type field; we retain the original term for
compatibility.  The variant field consists of a variable number of
the most significant bits of octet 8 of the UUID.

{{table1}} lists the contents of the variant field, where
the letter "x" indicates a "don't-care" value.

| Msb0 | Msb1 | Msb2 | Msb3 | Variant |Description                                                                    |
|    0 |    x | x    | x    | 1-7     |Reserved, NCS backward compatibility and includes Nil UUID as per {{niluuid}}. |
|    1 |    0 | x    | x    | 8-9,A-B |The variant specified in this document.                                        |
|    1 |    1 | 0    | x    | C-D     |Reserved, Microsoft Corporation backward compatibility.                        |
|    1 |    1 | 1    | x    | E-F     |Reserved for future definition and includes Max UUID as per {{maxuuid}}.       |
{: #table1 title='UUID Variants'}

Interoperability, in any form, with variants other than the one
defined here is not guaranteed but is not likely to be an issue in
practice.

Specifically for UUIDs in this document, bits 64 and 65 of the UUID (bits 0 and 1 of octet 8) MUST be set to 1 and 0 as specified in row 2 of {{table1}}.
Accordingly, all bit and field layouts avoid the use of these bits.

## Version Field {#version_field}
The version number is in the most significant 4 bits of octet 6
(bits 48 through 51 of the UUID).

{{table2}} lists all of the versions for this UUID variant 10xx specified in this document.

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
{: #table2 title='UUID variant 10xx versions defined by this specification'}

An example version/variant layout for UUIDv4 follows the table
where M represents the version placement for the hexadecimal representation of 0x4 (0b0100)
and the N represents the variant placement for one of the four possible hexadecimal representation of variant 10xx:
0x8 (0b1000), 0x9 (0b1001), 0xA (0b1010), 0xB (0b1011)

~~~~
00000000-0000-4000-8000-000000000000
00000000-0000-4000-9000-000000000000
00000000-0000-4000-A000-000000000000
00000000-0000-4000-B000-000000000000
xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
~~~~
{: title='UUIDv4 Variant Examples'}

It should be noted that the other remaining UUID variants found in {{table1}} leverage different sub-typing/versioning mechanisms.
The recording and definition of the remaining UUID variant and sub-typing combinations are outside of the scope of this document.

# UUID Layouts {#layout}

To minimize confusion about bit assignments within octets and among differing versions, the UUID record definition is provided as a grouping of fields within a bit layout consisting of four octets per row.
The fields are presented with the most significant one first.

## UUID Version 1 {#uuidv1}
UUID version 1 is a time-based UUID featuring a 60 bit timestamp
represented by Coordinated Universal Time (UTC) as a count of 100-
nanosecond intervals since 00:00:00.00, 15 October 1582 (the date of
Gregorian reform to the Christian calendar).

UUIDv1 also features a clock sequence field which is used to help avoid
duplicates that could arise when the clock is set backwards in time
or if the node ID changes.

The node field consists of an IEEE 802 MAC
address, usually the host address or a randomly derived value per {{unguessability}} and {{unidentifiable}}.

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
  Occupies bits 0 through 31 (octets 0-3).

time_mid:
: The middle 16 bits of the 60 bit starting timestamp.
  Occupies bits 32 through 47 (octets 4-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0001 (1).
  Occupies bits 48 through 51 of octet 6.

time_high:
: 12 bits that will contain the most significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

clock_seq:
: The 14 bits containing the clock sequence.
  Occupies bits 66 through 79 (octets 8-9).

node:
: 48 bit spatially unique identifier.
  Occupies bits 80 through 127 (octets 10-15).

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
the clock sequence associated with the changed node ID were known, then
the clock sequence MAY be incremented, but that is unlikely.

The clock sequence MUST be originally (i.e., once in the lifetime of
a system) initialized to a random number to minimize the correlation
across systems.  This provides maximum protection against node
identifiers that may move or switch from system to system rapidly.
The initial value MUST NOT be correlated to the node identifier.

Notes about IEEE 802 derived nodes:

{: spacing="compact"}

- Systems with multiple IEEE 802 addresses, any available one MAY be used.
- Systems with no IEEE address, a randomly or pseudo-randomly generated value MUST be used; see {{unguessability}} and {{unidentifiable}}.
- Systems utilizing a 64 bit MAC address the least significant, right-most 48 bits MAY be used.
- Systems utilizing an IEEE 802.15.4 16 bit address SHOULD instead utilize their 64 bit MAC address where least significant, right-most 48 bits MAY be used. An alternative is to generate 32 bits of random data and postfix at the end of the 16 bit MAC address to create a 48 bit value.

## UUID Version 2 {#uuidv2}
UUID version 2 is known as DCE Security UUIDs {{C309}} and {{C311}}.
As such, the definition of these UUIDs is outside the scope of this specification.

## UUID Version 3 {#uuidv3}
UUID version 3 is meant for generating UUIDs from "names"
that are drawn from, and unique within, some "namespace" as per {{name_based_uuid_generation}}.

UUIDv3 values are created by computing an MD5 {{RFC1321}}
hash over a given namespace value concatenated with the desired name value
after both have been converted to a canonical sequence of octets, as defined by the standards or conventions of its namespace, in network byte order.
This MD5 value is then used to populate all 128 bits of the UUID layout.
The UUID version and variant then replace the respective bits as defined by {{version_field}} and {{variant_field}}. An example of this bit substitution can be found in {{uuidv3_example}}.

Information around selecting a desired name's canonical format within a given namespace can be found in {{name_based_uuid_generation}}, "A note on names".

Some common namespace values have been defined via {{namespaces}}.

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
  from the computed MD5 value. Occupies bits 0 through 47 (octets 0-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0011 (3).
  Occupies bits 48 through 51 of octet 6.

md5_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following md5_high
  from the computed MD5 value.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

md5_low:
: The final 62 bits of the layout immediately following the var field to be
  filled with the least-significant, right-most bits of the final 64 bits
  from the computed MD5 value. Occupies bits 66 through 127 (octets 8-15)

## UUID Version 4 {#uuidv4}
UUID version 4 is meant for generating UUIDs from truly-random or
pseudo-random numbers.

An implementation may generate 128 bits of random data which is
used to fill out the UUID fields in {{uuidv4fields}}. The UUID version
and variant then replace the respective bits as defined by {{version_field}}
and {{variant_field}}.

Alternatively, an implementation MAY choose to randomly generate the exact required number of bits for
random_a, random_b, and random_c (122 bits total), and then concatenate the version and variant in the required position.

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
: The first 48 bits of the layout that can be filled with random data as specified in {{unguessability}}. Occupies bits 0 through 47 (octets 0-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0100 (4).
  Occupies bits 48 through 51 of octet 6.

random_b:
: 12 more bits of the layout that can be filled random data as per {{unguessability}}. Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

random_c:
: The final 62 bits of the layout immediately following the var field to be
  filled with random data as per {{unguessability}}. Occupies bits 66 through 127 (octets 8-15).

## UUID Version 5 {#uuidv5}
UUID version 5 is meant for generating UUIDs from "names"
that are drawn from, and unique within, some "namespace" as per {{name_based_uuid_generation}}.

UUIDv5 values are created by computing an SHA-1 {{FIPS180-4}}
hash over a given namespace value concatenated with the desired name value
after both have been converted to a canonical sequence of octets, as defined by the standards or conventions of its namespace, in network byte order.
The most significant, left-most 128 bits of the SHA-1 value is then used to populate all 128 bits of the UUID layout and the remaining 32 least significant, right-most bits of SHA-1 output are discarded.
The UUID version and variant then replace the respective bits as defined by {{version_field}} and {{variant_field}}. An example of this bit substitution and discarding exess bits can be found in {{uuidv5_example}}.

Information around selecting a desired name's canonical format within a given namespace can be found in {{name_based_uuid_generation}}, "A note on names".

Some common namespace values have been defined via {{namespaces}}.

There may be scenarios, usually depending on organizational security policies, where SHA-1 libraries may not be available or deemed unsafe for use.
As such, it may be desirable to generate name-based UUIDs derived from SHA-256 or newer SHA methods. These name-based UUIDs MUST NOT utilize UUIDv5 and MUST be within the UUIDv8 space defined by {{v8}}.
For implementation guidance around utilizing UUIDv8 for name-based UUIDs refer to the sub-section of {{name_based_uuid_generation}}.

For more information on SHA-1 security considerations see {{RFC6194}}.

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
  from the computed SHA-1 value.
  Occupies bits 0 through 47 (octets 0-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0101 (5).
  Occupies bits 48 through 51 of octet 6.

sha1_mid:
: 12 more bits of the layout consisting of the least significant,
  right-most 12 bits of 16 bits immediately following sha1_high
  from the computed SHA-1 value.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

sha1_low:
: The final 62 bits of the layout immediately following the var field to be
  filled by skipping the 2 most significant, left-most bits of the remaining SHA-1 hash
  and then using the next 62 most significant, left-most bits.
  Any leftover SHA-1 bits are discarded and unused. Occupies bits 66 through 127 (octets 8-15).

## UUID Version 6 {#uuidv6}

UUID version 6 is a field-compatible version of UUIDv1 {{uuidv1}}, reordered for improved
DB locality.
It is expected that UUIDv6 will primarily be used in contexts where UUIDv1 is used.
Systems that do not involve legacy UUIDv1 SHOULD use UUIDv7 instead.

Instead of splitting the timestamp into the low, mid, and high sections from
UUIDv1, UUIDv6 changes this sequence so timestamp bytes are stored from most
to least significant.
That is, given a 60 bit timestamp value as specified for UUIDv1 in {{uuidv1}},
for UUIDv6, the first 48 most significant bits are stored
first, followed by the 4 bit version (same position), followed by the remaining
12 bits of the original 60 bit timestamp.

The clock sequence  and node bits remain unchanged from their position in {{uuidv1}}.

The clock sequence and node bits SHOULD be reset to a pseudo-random value for each new UUIDv6 generated; however, implementations MAY choose to retain the old clock sequence and MAC address behavior from {{uuidv1}}. For more information on MAC address usage within UUIDs see the {{Security}}.

The format for the 16-byte, 128 bit UUIDv6 is shown in {{v6layout}}.


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
  Occupies bits 0 through 31 (octets 0-3).

time_mid:
: The middle 16 bits of the 60 bit starting timestamp.
  Occupies bits 32 through 47 (octets 4-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0110 (6).
  Occupies bits 48 through 51 of octet 6.

time_low:
: 12 bits that will contain the least significant 12 bits from the 60 bit starting timestamp.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

clock_seq:
: The 14 bits containing the clock sequence.
  Occupies bits 66 through 79 (octets 8-9).

node:
: 48 bit spatially unique identifier.
  Occupies bits 80 through 127 (octets 10-15).

With UUIDv6, the steps for splitting the timestamp into time_high and time_mid
are OPTIONAL
since the 48 bits of time_high and time_mid will remain in the same order.
An extra step of splitting the first 48 bits of the timestamp into the most
significant
32 bits and least significant 16 bits proves useful when reusing an existing
UUIDv1 implementation.


## UUID Version 7 {#v7}

UUID version 7 features a time-ordered value field derived from the widely
implemented and well known Unix Epoch timestamp source, the number of milliseconds
since midnight 1 Jan 1970 UTC, leap seconds excluded.
UUIDv7 generally has improved entropy characteristics over UUIDv1 {{uuidv1}} or UUIDv6 {{uuidv6}}.

UUIDv7 values are created by allocating a Unix timestamp in milliseconds in the most significant 48 bits and filling the remaining 74 bits, excluding the required version and variant bits, with random bits for each new UUIDv7 generated to provide uniqueness as per {{unguessability}}. Alternatively, implementations MAY fill the 74 bits, jointly, with a combination of the following subfields, in this order from the most significant bits to the least, to guarantee additional monotonicity within a millisecond:

1.  An OPTIONAL sub-millisecond timestamp fraction (12 bits at maximum) as per {{monotonicity_counters}} (Method 3).
2.  An OPTIONAL carefully seeded counter as per {{monotonicity_counters}} (Method 1 or 2).
3.  Random data for each new UUIDv7 generated for any remaining space.

Implementations SHOULD utilize UUIDv7 instead of UUIDv1 and UUIDv6 if
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
: 48 bit big-endian unsigned number of Unix epoch timestamp in milliseconds as
  per {{timestamp_considerations}}.
  Occupies bits 0 through 47 (octets 0-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b0111 (7).
  Occupies bits 48 through 51 of octet 6.

rand_a:
: 12 bits pseudo-random data to provide uniqueness as per {{unguessability}}
  and/or optional constructs to guarantee additional monotonicity as
  per {{monotonicity_counters}}.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

rand_b:
: The final 62 bits of pseudo-random data to provide uniqueness as per {{unguessability}}
  and/or an optional counter to guarantee additional monotonicity as per {{monotonicity_counters}}.
  Occupies bits 66 through 127 (octets 8-15).

## UUID Version 8 {#v8}

UUID version 8 provides an RFC-compatible format for experimental or vendor-specific
use cases.
The only requirement is that the variant and version bits MUST be set as
defined in {{variant_field}} and {{version_field}}.
UUIDv8's uniqueness will be implementation-specific and MUST NOT be assumed.

The only explicitly defined bits are those of the version and variant fields, leaving 122
bits
for implementation specific UUIDs. To be clear:
UUIDv8 is not a replacement for UUIDv4 {{uuidv4}} where all 122 extra bits are
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
  fit. Occupies bits 0 through 47 (octets 0-5).

ver:
: The 4 bit version field as defined by {{version_field}}, set to 0b1000 (8).
  Occupies bits 48 through 51 of octet 6.

custom_b:
: 12 more bits of the layout that can be filled as an implementation sees fit.
  Occupies bits 52 through 63 (octets 6-7).

var:
: The 2 bit variant field as defined by {{variant_field}}, set to 0b10.
  Occupies bits 64 and 65 of octet 8.

custom_c:
: The final 62 bits of the layout immediately following the var field to be
  filled as an implementation sees fit.
  Occupies bits 66 through 127 (octets 8-15).

## Nil UUID {#niluuid}
The nil UUID is special form of UUID that is specified to have all
128 bits set to zero.

~~~~
00000000-0000-0000-0000-000000000000
~~~~
{: title='Nil UUID Format'}

A Nil UUID value can be useful to communicate the absence of any other UUID value in situations that otherwise require or use a 128 bit UUID.  A Nil UUID can express the concept "no such value here". Thus it is reserved for such use as needed for implementation-specific situations.

## Max UUID {#maxuuid}

The Max UUID is a special form of UUID that is specified to have all 128 bits
set to 1. This UUID can be thought of as the inverse of Nil UUID defined
in {{niluuid}}.

~~~~
FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF
~~~~
{: title='Max UUID Format'}

A Max UUID value can be used as a sentinel value in situations where a 128 bit UUID is required but a concept such as "end of UUID list" needs to be expressed, and is reserved for such use as needed for implementation-specific situations.

# UUID Best Practices {#uuid_best_practices}

The minimum requirements for generating UUIDs are
described in this document for each version.
Everything else is an implementation detail and it is
up to the implementer to decide what is appropriate for a given
implementation. Various relevant factors are covered
below to help guide an implementer through the different trade-offs among
differing UUID implementations.

## Timestamp Considerations {#timestamp_considerations}

UUID timestamp source, precision, and length was the topic of great debate
while creating UUIDv7 for this specification. Choosing the right timestamp for
your application is a very important topic. This section will detail some
of the most common points on this topic.

{: vspace='0'}

Reliability:
: Implementations acquire the current timestamp from a reliable source to
  provide values that are time-ordered and continually increasing.
  Care must be taken to ensure that timestamp changes from the environment
  or operating system are handled in a way that is consistent with implementation
  requirements.
  For example, if it is possible for the system clock to move backward due
  to either manual adjustment or corrections from a time synchronization protocol,
  implementations need to determine how to handle such cases. (See Altering, Fuzzing,
  or Smearing below.)

Source:
: UUID version 1 and 6 both utilize a Gregorian epoch timestamp while UUIDv7
  utilizes a Unix Epoch timestamp. If other timestamp sources or a custom timestamp
  epoch are required, UUIDv8 MUST be used.

Sub-second Precision and Accuracy:
: Many levels of precision exist for timestamps: milliseconds, microseconds,
  nanoseconds, and beyond.
  Additionally fractional representations of sub-second precision may be desired
  to mix various levels of precision in a time-ordered manner.
  Furthermore, system clocks themselves have an underlying granularity and
  it is frequently less than the precision offered by the operating system.
  With UUID version 1 and 6, 100-nanoseconds of precision are present while
  UUIDv7 features millisecond level of precision by default within the Unix epoch
  that does not exceed the granularity capable in most modern systems.
  For other levels of precision UUIDv8 is available.
  Similar to {{monotonicity_counters}}, with UUIDv1 or UUIDv6,
  a high resolution timestamp can be simulated by keeping a count of
  the number of UUIDs that have been generated with the same value of
  the system time, and using it to construct the low order bits of the
  timestamp.  The count of the high resolution timestamp will range between zero and the number of
  100-nanosecond intervals per system time interval.

Length:
: The length of a given timestamp directly impacts how many timestamp ticks can be contained in a UUID before the maximum
  value for the timestamp field is reached.
  Take care to ensure that the proper length is selected for a given
  timestamp.
  UUID version 1 and 6 utilize a 60 bit timestamp valid until 5623 AD and UUIDv7 features a 48
  bit timestamp valid until the year 10889 AD.

Altering, Fuzzing, or Smearing:
: Implementations MAY alter the actual timestamp. Some examples include security
  considerations around providing a real clock value within a UUID, to correct
  inaccurate clocks, to handle leap seconds, or instead of dividing a number of microseconds by 1000 to obtain a millisecond value; dividing by 1024 (or some other value) for performance reasons. This specification makes no
  requirement or guarantee about how close the clock value needs to be to the actual
  time.
  If UUIDs do not need to be frequently generated, the UUIDv1 or UUIDv6 timestamp can
  simply be the system time multiplied by the number of 100-nanosecond
  intervals per system time interval.

Padding:
: When timestamp padding is required, implementations MUST pad the most significant
  bits (left-most) bits with data. An example for this padding data is to fill the most significant,
  left-most bits of a Unix timestamp with zeroes to complete the 48
  bit timestamp in UUIDv7. An alternative approach for padding data is to fill the most significant, left-most bits with the number of 32 bit Unix timestamp roll-overs after 2038-01-19.

Truncating:
: When timestamps need to be truncated, the lower, least significant
  bits MUST be used. An example would be truncating a 64 bit Unix timestamp
  to the least significant, right-most 48 bits for UUIDv7.

Error Handling:
: If a system overruns the generator by requesting too many UUIDs
  within a single system time interval, the UUID service can
  return an error, or stall the UUID generator until the system clock
  catches up, and MUST NOT return knowingly duplicate values due to a
  counter rollover.
  Note that if the processors overrun the UUID generation frequently,
  additional node identifiers can be allocated to the system, which
  will permit higher speed allocation by making multiple UUIDs
  potentially available for each time stamp value.
  Similar techniques are discussed in {{distributed_shared_knowledge}}.

## Monotonicity and Counters {#monotonicity_counters}

Monotonicity (each subsequent value being greater than the last) is the backbone of time-based sortable UUIDs. Normally, time-based
UUIDs from this document will be monotonic due to an embedded timestamp; however,
implementations can guarantee additional monotonicity via the concepts covered
in this section.

Take care to ensure UUIDs generated in batches are
also monotonic. That is, if one thousand UUIDs are generated for the same
timestamp, there should be sufficient logic for organizing the creation order of
those one thousand UUIDs.
Batch UUID creation implementations MAY utilize a monotonic counter that
increments for each UUID created during a given timestamp.

For single-node UUID implementations that do not need to create batches of
UUIDs, the embedded timestamp within UUID version 6 and 7 can provide
sufficient monotonicity guarantees by simply ensuring that timestamp increments
before creating a new UUID. Distributed nodes are discussed in
{{distributed_shared_knowledge}}.

Implementations SHOULD employ the following methods for single-node UUID implementations
that require batch UUID creation, or are otherwise concerned about monotonicity
with high frequency UUID generation.

{: vspace='0'}

Fixed-Length Dedicated Counter Bits (Method 1):
: Some implementations allocate a specific number of bits in the
  UUID layout to the sole purpose of tallying the total number of UUIDs created
  during a given UUID timestamp tick.
  A fixed bit-length counter, if present, MUST be positioned immediately after the
  embedded timestamp. This promotes sortability and allows random data generation
  for each counter increment.
  With this method, the rand_a section (or a subset of its left-most bits) of UUIDv7
  is used as fixed-length dedicated counter bits that are incremented for
  every UUID generation.
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
  The increment value for every UUID generation is a random integer
  of any desired length larger than zero. It ensures the UUIDs retain the required
  level of unguessability provided by the underlying entropy.
  The increment value MAY be 1 when the number of UUIDs generated in a particular
  period of time is important and guessability is not an issue. However, incrementing the counter by 1
  SHOULD NOT be used by implementations that favor unguessability, as the resulting
  values are easily guessable.

Replace Left-Most Random Bits with Increased Clock Precision (Method 3):
: For UUIDv7, which has millisecond timestamp precision, it is possible
  to use additional clock precision available on the system to substitute
  for up to 12 random bits immediately following the timestamp.  This can provide
  values that are time-ordered with sub-millisecond precision, using
  however many bits are appropriate in the implementation environment.
  With this method, the additional time precision bits MUST follow the
  timestamp as the next available bit, in the rand_a field for UUIDv7.

  To calculate this value, start with the portion of the timestamp
  expressed as a fraction of clock's tick value (fraction of a millisecond
  for UUIDv7).  Compute the count of possible values that can be represented in
  the available bit space, 4096 for the UUIDv7 rand_a field.
  Using floating point or scaled integer arithmetic, multiply this fraction of a millisecond
  value by 4096 and round down (toward zero) to an integer result to arrive at a number
  between 0 and the maximum allowed for the indicated bits
  which sorts monotonically based on time. Each increasing fractional
  value will result in an increasing bit field value, to the
  precision available with these bits.

  For example, let's assume a system timestamp of 1 Jan 2023 12:34:56.1234567.
  Taking the precision greater than 1ms gives us a value of 0.4567, as a
  fraction of a millisecond.  If we wish to encode this as 12 bits, we can
  take the count of possible values that fit in those bits (4096, or 2 to the 12th power)
  and multiply it by our millisecond fraction value of 0.4567 and truncate the result to
  an integer, which gives an integer value of 1870. Expressed as hexadecimal it is
  0x74E, or the binary bits 0b011101001110.  One can then use those 12 bits
  as the most significant (left-most) portion of the random section of the UUID
  (e.g., the rand_a field in UUIDv7).
  This works for any desired bit length that fits into a UUID, and applications
  can decide the appropriate length based on available clock precision, but for
  UUIDv7, it is limited to 12 bits at maximum to reserve sufficient space for
  random bits.

  The main benefit to encoding additional timestamp precision
  is that it utilizes additional time precision already available in the system clock
  to provide values that are more likely to be unique, and thus may simplify
  certain implementations. This technique can also be used in conjunction with one
  of the other methods, where this additional time precision would immediately
  follow the timestamp, and then if any bits are to be used as clock sequence
  they would follow next.

The following sub-topics cover topics related solely with creating reliable
fixed-length dedicated counters:

{: vspace='0'}

Fixed-Length Dedicated Counter Seeding:
: Implementations utilizing the fixed-length counter method randomly initialize
  the counter with each new timestamp tick.
  However, when the timestamp has not increased, the counter is instead incremented by the desired increment logic.
  When utilizing a randomly seeded counter alongside Method 1, the random value MAY
  be regenerated with each counter increment without impacting sortability.
  The downside is that Method 1 is prone to overflows if a counter of adequate
  length is not selected or the random data generated leaves little room for
  the required number of increments.
  Implementations utilizing fixed-length counter method MAY also choose to
  randomly initialize a portion of the counter rather than the entire counter. For
  example, a 24 bit counter could have the 23 bits in least-significant, right-most,
  position randomly initialized. The remaining most significant, left-most
  counter bit is initialized as zero for the sole purpose of guarding against
  counter rollovers.

Fixed-Length Dedicated Counter Length:
: Select a counter bit-length that can properly handle
  the level of timestamp precision in use.
  For example, millisecond precision generally requires a larger counter than a
  timestamp with nanosecond precision.
  General guidance is that the counter SHOULD be at least 12 bits but no longer
  than 42 bits.
  Care must be taken to ensure that the counter length selected leaves
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
  by ensuring that the total length of a possible increment in the least significant,
  right most position is less than the total length of the random value being incremented.
  As such, the most significant, left-most, bits can be incremented as rollover
  guarding.

Counter Rollover Handling:
: Counter rollovers MUST be handled by the application to avoid sorting issues.
  The general guidance is that applications that care about absolute monotonicity
  and sortability should freeze the counter and wait for the timestamp to advance
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
: Implementations SHOULD check if the currently generated UUID is greater
than the previously generated UUID. If this is not the case then any number
of things could have occurred, such as clock rollbacks,
leap second handling, and counter rollovers. Applications SHOULD embed sufficient
logic to catch these scenarios and correct the problem to ensure that the next
UUID generated is greater than the previous, or at least report an appropriate error.
To handle this scenario, the
general guidance is that application MAY reuse the previous timestamp and
increment the previous counter method.

## UUID Generator States {#generator_states}

The (optional) UUID generator state only needs to be read from stable storage once at boot
time, if it is read into a system-wide shared volatile store (and
updated whenever the stable store is updated).

This stable storage MAY be used to record various portions of the UUID generation
which prove useful for batch UUID generation purposes and monotonic error checking with UUIDv6 and UUIDv7.
These stored values include but are not limited to last known timestamp, clock sequence, counters, and random data.

If an implementation does not have any stable store available, then
it MAY proceed with UUID generation as if this was the first UUID created within a batch.
This is the least desirable implementation because it will increase the frequency
of creation of values such as clock sequence, counters, or random data, which increases the
probability of duplicates. Further, frequent generation of random numbers also puts more stress on any entropy source and or entropy pool being used as the basis for such random numbers.

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

This section will detail the two additional collision resistance approaches that have been observed by multi-node
UUID implementations in distributed environments.

It should be noted that, although this section details two methods for the sake of completeness,
implementations should utilize the pseudo-random Node ID option if additional collision resistance for distributed UUID generation is a requirement.
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
be willing to rely on the random number source at all hosts.

## Name-Based UUID Generation {#name_based_uuid_generation}
The requirements for name-based UUIDs are as follows:

* UUIDs generated at different times from the same name (using the same canonical format) in the
  same namespace MUST be equal.

* UUIDs generated from two different names (same or differing canonical format) in the same namespace
  should be different (with very high probability).

* UUIDs generated from the same name (same or differing canonical format) in two different namespaces
  should be different (with very high probability).

* If two UUIDs that were generated from names (using the same canonical format) are equal, then they
  were generated from the same name in the same namespace (with very
  high probability).

{: vspace='0'}

A note on names:
: The concept of name (and namespace) should be broadly construed and not limited to textual names. A canonical sequence of octets is one that conforms to the specification for that name form's canonical representation. A name can have many usual forms, only one of which can be canonical. An implementer of new namespaces for UUIDs needs to reference the specification for the canonical form of names in that space, or define such a canonical for the namespace if it does not exist.
  For example, at the time of this specification, {{RFC8499}} domain name system (DNS) has three conveyance formats: common (www.example.com), presentation (www.example.com.) and wire format (3www7example3com0).
  Looking at {{X500}} distinguished names (DNs), the previous version of this specification allowed either text based or binary distinguished encoding rules (DER) based names as inputs.
  For {{RFC1738}} uniform resource locators (URLs), one could provide a fully-qualified domain-name (FQDN) with or without the protocol identifier (www.example.com) or (https://www.example.com).
  When it comes to {{X660}} object identifiers (OIDs) one could choose dot-notation without the leading dot (2.999), choose to include the leading dot (.2.999) or select one of the many formats from {{X680}} such as OID Internationalized Resource Identifier (OID-IRI) (/Joint-ISO-ITU-T/Example).
  While most users may default to the common format for DNS, FQDN format for a URL, text format for X.500 and dot-notation without a leading dot for OID; name-based UUID implementations generally SHOULD allow arbitrary input which will compute name-based UUIDs for any of the aforementioned example names and others not defined here.
  Each name format within a namespace will output different UUIDs. 
  As such, the mechanisms or conventions used for allocating names and ensuring their uniqueness within their namespaces are beyond the scope of this specification.

A note on namespaces:
: While {{namespaces}} details a few interesting namespaces; implementations SHOULD provide the ability to input a custom namespace.
  For example, any other UUID MAY be generated and used as the desired namespace input for a given application context to
  ensure all names created are unique within the newly created namespace.

Name-based UUIDs using UUIDv8:
: As per {{uuidv5}} name-based UUIDs that desire to use modern hashing algorithms MUST be created within the UUIDv8 space.
 These MAY leverage newer hashing protocols such as SHA-256 or SHA-512 defined by {{FIPS180-4}}, SHA-3 or SHAKE defined by {{FIPS202}}, or even protocols that have not been defined yet.
 To ensure UUIDv8 name-based UUID values of different hashing protocols can exist in the same bit space; this document defines various "hashspaces" in {{hashspaces}}.
 Creation of name-based UUID values using UUIDv8 follows the same logic defined in {{uuidv5}}, but the hashspace should be used as the starting point with the desired
 namespace and name concatenated to the end of the hashspace.
 Then an implementation may apply the desired hashing algorithm to the entire value after all have been converted to a canonical sequence of octets, as defined by the standards or conventions of its namespace, in network byte order.
 Ensure that the version and variant bits are modified as per {{v8}} bit layout, and finally trim any excess bits beyond 128.
 An important note for secure hashing algorithms that produce outputs of an arbitrary size, such as those found in SHAKE, the output hash MUST be 128 bits or larger.
 See {{uuidv8_example_name}} for a SHA-256 UUIDv8 example test vector.

Advertising the Hash Algorithm:
: Name-based UUIDs utilizing UUIDv8 do not allocate any available bits to identifying the hashing algorithm.
  As such where common knowledge about the hashing algorithm for a given UUIDv8 name-based UUID is required, sharing the hashspace ID from {{hashspaces}} proves useful for identifying the algorithm.
  That is, to detail that SHA-256 was used to create a given UUIDv8 name-based UUID, an implementation may also share the "3fb32780-953c-4464-9cfd-e85dbbe9843d" hashspace which uniquely identifies the SHA-256 hashing algorithm for the purpose of UUIDv8. Mind you that this need not be the only method of sharing the hashing algorithm; this is one example of how two systems could share knowledge.
  The protocol of choice, communication channels, and actual method of sharing this data between systems are outside the scope of this specification.

## Collision Resistance {#collision_resistance}

Implementations should weigh the consequences of UUID collisions within their
application and when deciding between UUID versions that use entropy (randomness)
versus the other components such as those in {{timestamp_considerations}} and {{monotonicity_counters}}.
This is especially true for distributed node collision resistance as defined
by {{distributed_shared_knowledge}}.

There are two example scenarios below which help illustrate the varying seriousness
of a collision within an application.

{: vspace='0'}

Low Impact:
: A UUID collision generated a duplicate log entry which results in incorrect
  statistics derived from the data. Implementations that are not negatively
  affected by collisions may continue with the entropy and uniqueness provided
  by the traditional UUID format.

High Impact:
: A duplicate key causes an airplane to receive the wrong course which puts
  people's lives at risk. In this scenario there is no margin for error. Collisions
  must be avoided and failure is unacceptable. Applications dealing with this
  type of scenario must employ as much collision resistance as possible within
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
uniqueness for practical implementation purposes.
Implementations MAY implement a shared knowledge scheme introduced in {{distributed_shared_knowledge}} as they see fit to extend the uniqueness guaranteed by this specification.


## Unguessability {#unguessability}
Implementations SHOULD utilize a cryptographically secure pseudo-random number
generator (CSPRNG) to provide values that are both difficult to predict ("unguessable")
and have a low likelihood of collision ("unique").  The exception is when a
suitable CSPRNG is unavailable in the execution environment.
Take care to ensure the CSPRNG state is properly reseeded upon
state changes, such as process forks, to ensure proper CSPRNG operation.
CSPRNG ensures the best of {{collision_resistance}} and {{Security}} are present in modern UUIDs.

Further advice on generating cryptographic-quality random numbers can be found in {{RFC4086}}, {{RFC8937}} and in {{RANDOM}}.

## UUIDs That Do Not Identify the Host {#unidentifiable}
This section describes how to generate a UUIDv1 or UUIDv6 value if an IEEE
802 address is not available, or its use is not desired.

Implementations MAY leverage MAC address randomization techniques (IEEE 802.11bh) as an alternative to the pseudo-random logic provided in this section.

Alternatively, implementations MAY elect to obtain a 48 bit cryptographic-quality random
number as per {{unguessability}} to use it as the node ID.
After generating the 48 bit fully randomized node value, implementations MUST set the least significant bit of the first octet of the node ID set to 1.
This bit is the unicast/multicast bit, which will never be set in IEEE 802
addresses obtained from network cards.  Hence, there can never be a
conflict between UUIDs generated by machines with and without network
cards.
An example of generating a randomized 48 bit node value and the subsequent bit modification is detailed in the {{test_vectors}} appendix.
For more information about IEEE 802 address and the unicast/multicast or local/global bits please review {{RFC7042}}.

For compatibility with earlier specifications, note that this
document uses the unicast/multicast bit, instead of the arguably more
correct local/global bit because MAC addresses with the local/global bit set or not are both possible in a network.
This is not the case with the unicast/multicast bit.
One node cannot have a MAC address that multicasts to multiple nodes.

In addition, items such as the computer's name and the name of the
operating system, while not strictly speaking random, will help
differentiate the results from those obtained by other systems.

The exact algorithm to generate a node ID using these data is system
specific, because both the data available and the functions to obtain
them are often very system specific.  A generic approach, however, is
to accumulate as many sources as possible into a buffer, use a
message digest (such as SHA-256 or SHA-512 defined by {{FIPS180-4}}), take an arbitrary 6
bytes from the hash value, and set the multicast bit as described
above.

## Sorting {#sorting}

UUIDv6 and UUIDv7 are designed so that implementations that require sorting
(e.g., database indexes) sort as opaque raw bytes, without need for
parsing or introspection.

Time ordered monotonic UUIDs benefit from greater database index locality
because the new values are near each other in the index.
As a result objects are more easily clustered together for better performance.
The real-world differences in this approach of index locality vs random data
inserts can be one order of magnitude or more.

UUID formats created by this specification are intended to be lexicographically sortable
while in the textual representation.

UUIDs created by this specification are crafted with big-endian byte order
(network byte order) in mind. If little-endian style is required, UUIDv8
is available for custom UUID formats.


## Opacity {#opacity}
As general guidance, it is recommend to avoid parsing UUID values unnecessarily,
and instead treating UUIDs as opaquely as possible.  Although application-specific
concerns could of course require some degree of introspection
(e.g., to examine the {{variant_field}}, {{version_field}} or perhaps the timestamp of a UUID),
the advice here is to avoid this or other parsing unless absolutely necessary.
Applications typically tend to be simpler, more interoperable, and perform better,
when this advice is followed.

## DBMS and Database Considerations {#database_considerations}

For many applications, such as databases, storing UUIDs as text is unnecessarily
verbose, requiring 288 bits to represent 128 bit UUID values.
Thus, where feasible, UUIDs SHOULD be stored within database applications
as the underlying 128 bit binary value.

For other systems, UUIDs MAY be stored in binary form or as text, as appropriate.
The trade-offs to both approaches are:


* Storing as binary requires less space and may result in faster data access.



* Storing as text requires more space but may require less translation if the
  resulting text form is to be used after retrieval, which thus may make it simpler
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
All references to {{RFC4122}} in the IANA registries should be replaced with references to this document.
References to {{RFC4122}} document's Section 4.1.2 should be updated to refer to this document's {{format}}.

The IANA URN namespace registration {{URNNamespaces}} for UUID filed in {{RFC4122}} should be updated to reference this document.

Finally IANA should track UUID Variants, UUID Subtypes, and Special Case "Reserved UUIDs" such as Nil, Max, and Namespace IDs as specified in {{iana1}}, {{iana2}}, {{iana3}}.

The policy for these three registries is "Specification Required", per {{RFC8126}}, Section 4.6.

When evaluating requests, the designated expert(s) should consider community feedback, how well-defined is the reference specification, and this specification's requirements.
Vendor-specific, application-specific, and deployment-specific values are unable to be registered.
Specification documents should be published in a stable, freely available manner (ideally located with a URL) but need not be standards.
The designated experts will either approve or deny the registration request, and communicate their decision to IANA. Denials should include an explanation and, if applicable, suggestions as to how to make the request successful.

## IANA UUID Variants Registry and Registration {#iana1}
This specification defines the "UUID Variants" registry for common, widely used UUID standards.

{{ianaVariants}} should be used as-is for this registry with "This document" replaced as required.

| Name           | Bits | Variant | Reference                  |
| Apollo NCS     | 0xxx | 1-7     | {{RFC4122}}, This document |
| OSF DCE / IETF | 10xx | 8-9,A-B | {{RFC4122}}, This document |
| Microsoft      | 110x | C-D     | {{RFC4122}}, This document |
| Unused         | 111x | E-F     | {{RFC4122}}, This document |
{: #ianaVariants title='IANA UUID Variants'}

## IANA UUID Subtype Registry and Registration {#iana2}
This specification defines the "UUID Subtype" registry for common, widely used UUID standards.

{{ianaSubtypes}} should be used as-is for this registry with "This document" replaced as required.

| Name                           | ID | Hex | Subtype | Variant        | Reference                  |
| Unused                         |  0 | 0x0 | Version | OSF DCE / IETF | This document              |
| Gregorian Time-based           |  1 | 0x1 | Version | OSF DCE / IETF | {{RFC4122}}, This document |
| DCE Security                   |  2 | 0x2 | Version | OSF DCE / IETF | {{C309}}, {{C311}}         |
| MD5 Name-based                 |  3 | 0x3 | Version | OSF DCE / IETF | {{RFC4122}}, This document |
| Random                         |  4 | 0x4 | Version | OSF DCE / IETF | {{RFC4122}}, This document |
| SHA-1 Name-based               |  5 | 0x5 | Version | OSF DCE / IETF | {{RFC4122}}, This document |
| Reordered Gregorian Time-based |  6 | 0x6 | Version | OSF DCE / IETF | This document              |
| Unix Time-based                |  7 | 0x7 | Version | OSF DCE / IETF | This document              |
| Custom                         |  8 | 0x8 | Version | OSF DCE / IETF | This document              |
| Unspecified                    |  9 | 0x9 | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 10 | 0xA | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 11 | 0xB | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 12 | 0xC | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 13 | 0xD | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 14 | 0xE | Version | OSF DCE / IETF | This document              |
| Unspecified                    | 15 | 0xF | Version | OSF DCE / IETF | This document              |
{: #ianaSubtypes title='IANA UUID Subtypes'}

## IANA Reserved UUIDs Registry and Registration {#iana3}
This specification defines the "Reserved UUIDs" registry for common, widely used special purpose UUIDs to promote reuse.

{{ianaSubtypes}} should be used as-is for this registry with "This document" replaced as required.

| Name     | Type         | UUID                                 | Reference                  |
| Nil UUID | Special ID   | 00000000-0000-0000-0000-000000000000 | {{RFC4122}}, This document |
| Max UUID | Special ID   | FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF | This document              |
| DNS      | Namespace ID | 6ba7b810-9dad-11d1-80b4-00c04fd430c8 | {{RFC4122}}, This document |
| URL      | Namespace ID | 6ba7b811-9dad-11d1-80b4-00c04fd430c8 | {{RFC4122}}, This document |
| OID      | Namespace ID | 6ba7b812-9dad-11d1-80b4-00c04fd430c8 | {{RFC4122}}, This document |
| X500     | Namespace ID | 6ba7b814-9dad-11d1-80b4-00c04fd430c8 | {{RFC4122}}, This document |
{: #ianaReserved title='IANA Reserved UUIDs'}

# Security Considerations {#Security}

Implementations SHOULD NOT assume that UUIDs are hard to guess.
For example, they MUST NOT be used
as security capabilities (identifiers whose mere possession grants
access).  Discovery of predictability in a random number source will
result in a vulnerability.

Implementations MUST NOT assume that it is easy to determine if a UUID has been
slightly modified in order to redirect a reference to another
object.  Humans do not have the ability to easily check the integrity
of a UUID by simply glancing at it.

MAC addresses pose inherent security risks around privacy and SHOULD NOT be used within
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

See {{RFC6151}} for MD5 Security Considerations and {{RFC6194}} for SHA-1 security considerations.

# Acknowledgements {#Acknowledgements}

The authors gratefully acknowledge the contributions of Rich Salz,
Michael Mealling,
Ben Campbell,
Ben Ramsey,
Fabio Lima,
Gonzalo Salgueiro,
Martin Thomson,
Murray S. Kucherawy,
Rick van Rein,
Rob Wilton,
Sean Leonard,
Theodore Y. Ts'o,
Robert Kieffer,
Sergey Prokhorenko,
LiosK.

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

# Some Namespace IDs {#namespaces}
This appendix table, {{namespaceIDs}}, details the namespace IDs for some potentially interesting namespaces such those for
{{RFC8499}} domain name system (DNS), {{RFC1738}} uniform resource locators (URLs), {{X660}} object identifiers (OIDs), and {{X500}} distinguished names (DNs).

| Namespace | Namespace ID                         |
| DNS       | 6ba7b810-9dad-11d1-80b4-00c04fd430c8 |
| URL       | 6ba7b811-9dad-11d1-80b4-00c04fd430c8 |
| OID       | 6ba7b812-9dad-11d1-80b4-00c04fd430c8 |
| X500      | 6ba7b814-9dad-11d1-80b4-00c04fd430c8 |
{: #namespaceIDs title='Namespace IDs'}

Generally speaking, Namespace IDs are allocated as follows:

{: spacing="compact"}
- The first Namespace ID, for DNS, was calculated from a time-based UUIDv1 and "6ba7b810-9dad-11d1-80b4-00c04fd430c8" used as a starting point.
- Subsequent Namespace IDs increment the least-significant, right-most bit of time_low "6ba7b810" while freezing the rest of the UUID to "9dad-11d1-80b4-00c04fd430c8".
- New Namespace IDs MUST use this same logic and MUST NOT use a previously used Namespace ID value.
- Thus, "6ba7b815" is the next available time_low for a new Namespace ID with the full ID being "6ba7b815-9dad-11d1-80b4-00c04fd430c8".
- The upper bound for time_low in this special use, namespace ID, is "ffffffff" or "ffffffff-9dad-11d1-80b4-00c04fd430c8" which should be sufficient space for future namespace IDs.

Note that the Namespace ID "6ba7b813-9dad-11d1-80b4-00c04fd430c8" and its usage is not defined by this document or by {{RFC4122}}, as such it SHOULD NOT be used as a Namespace ID.

New Namespace IDs MUST be documented as per {{IANA}} and {{iana3}} if they are to be globally available and fully interoperable.
Implementations MAY continue to use vendor-specific, application-specific, and deployment-specific Namespace ID values but know that interoperability is not guaranteed.
These custom Namespace IDs MUST NOT use the logic above and instead are RECOMMENDED to use UUIDv4 or UUIDv8 values as identifiers.

# Some Hashspace IDs {#hashspaces}
This appendix lists some hashspace IDs for use with UUIDv8 name-based UUIDs.

~~~~ code
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
For the randomized node, the least significant bit of the first octet is set to a value of 1 as per {{unidentifiable}}. 
Thus the starting value 0x9E6BDECED846 was changed to 0x9F6BDECED846.

The pseudocode used for converting from a 64 bit Unix timestamp to a 100ns Gregorian timestamp value
has been left in the document for reference purposes.

~~~~ code
# Gregorian to Unix Offset:
# The number of 100-ns intervals between the
# UUID epoch 1582-10-15 00:00:00
# and the Unix epoch 1970-01-01 00:00:00
# Greg_Unix_offset = 0x01b21dd213814000 or 122192928000000000

# Unix 64 bit Nanosecond Timestamp:
# Unix NS: Tuesday, February 22, 2022 2:22:22 PM GMT-05:00
# Unix_64_bit_ns = 0x16D6320C3D4DCC00 or 1645557742000000000

# Unix Nanosecond precision to Gregorian 100-nanosecond intervals
# Greg_100_ns = (Unix_64_bit_ns/100)+Greg_Unix_offset

# Work:
# Greg_100_ns = (1645557742000000000/100)+122192928000000000
# Unix_64_bit_ns = (138648505420000000-122192928000000000)*100

# Final:
# Greg_100_ns = 0x1EC9414C232AB00 or 138648505420000000
~~~~
{: title='Test Vector Timestamp Pseudo-code'}

## Example of a UUIDv1 Value {#uuidv1_example}

~~~~
-------------------------------------------
field      bits value
-------------------------------------------
time_low   32   0xC232AB00
time_mid   16   0x9414
ver         4   0x1
time_high  12   0x1EC
var         2   0b10
clock_seq  14   0b11, 0x3C8
node       48   0x9F6BDECED846
-------------------------------------------
total      128
-------------------------------------------
final: C232AB00-9414-11EC-B3C8-9E6BDECED846
~~~~
{: title='UUIDv1 Example Test Vector'}

## Example of a UUIDv3 Value {#uuidv3_example}
The MD5 computation from is detailed in {{v3md5}} using the DNS NameSpace and the Name "www.example.com".
while the field mapping and all values are illustrated in {{v3fields}}.
Finally to further illustrate the bit swapping for version and variant see {{v3vervar}}.

~~~~
Namespace (DNS):  6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:             www.example.com
------------------------------------------------------
MD5:              5df418813aed051548a72f4a814cf09e
~~~~
{: id='v3md5' title='UUIDv3 Example MD5'}

~~~~
-------------------------------------------
field     bits value
-------------------------------------------
md5_high  48   0x5df418813aed
ver        4   0x3
md5_mid   12   0x515
var        2   0b10
md5_low   62   0b00, 0x8a72f4a814cf09e
-------------------------------------------
total     128
-------------------------------------------
final: 5df41881-3aed-3515-88a7-2f4a814cf09e
~~~~
{: id='v3fields' title='UUIDv3 Example Test Vector'}

~~~~
MD5 hex and dash:      5df41881-3aed-0515-48a7-2f4a814cf09e
Ver and Var Overwrite: xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                 5df41881-3aed-3515-88a7-2f4a814cf09e
~~~~
{: id='v3vervar' title='UUIDv3 Example Ver Var bit swaps'}

## Example of a UUIDv4 Value {#uuidv4_example}
This UUIDv4 example was created by generating 16 bytes
of random data resulting in the hexadecimal value of
919108F752D133205BACF847DB4148A8. This is then used to
fill out the fields as shown in {{v4fields}}.

Finally to further illustrate the bit swapping for version and variant see {{v4vervar}}.

~~~~
-------------------------------------------
field     bits value
-------------------------------------------
random_a  48   0x919108f752d1
ver        4   0x4
random_b  12   0x320
var        2   0b10
random_c  62   0b01, 0xbacf847db4148a8
-------------------------------------------
total     128
-------------------------------------------
final: 919108f7-52d1-4320-9bac-f847db4148a8
~~~~
{: id='v4fields' title='UUIDv4 Example Test Vector'}

~~~~
Random hex:            919108f752d133205bacf847db4148a8
Random hex and dash:   919108f7-52d1-3320-5bac-f847db4148a8
Ver and Var Overwrite: xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                 919108f7-52d1-4320-9bac-f847db4148a8
~~~~
{: id='v4vervar' title='UUIDv4 Example Ver/Var bit swaps '}


## Example of a UUIDv5 Value {#uuidv5_example}
The SHA-1 computation from is detailed in {{v5sha1}} using the DNS NameSpace and the Name "www.example.com".
while the field mapping and all values are illustrated in {{v5fields}}.
Finally to further illustrate the bit swapping for version and variant and the unused/discarded part of the SHA-1 value see {{v5vervar}}.

~~~~
Namespace (DNS):  6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:             www.example.com
----------------------------------------------------------
SHA-1:            2ed6657de927468b55e12665a8aea6a22dee3e35
~~~~
{: id='v5sha1' title='UUIDv5 Example SHA-1'}

~~~~
-------------------------------------------
field      bits value
-------------------------------------------
sha1_high  48   0x2ed6657de927
ver         4   0x5
sha1_mid   12   0x68b
var         2   0b10
sha1_low   62   0b01, 0x5e12665a8aea6a2
-------------------------------------------
total      128
-------------------------------------------
final: 2ed6657d-e927-568b-95e1-2665a8aea6a2
~~~~
{: id='v5fields' title='UUIDv5 Example Test Vector'}

~~~~
SHA-1 hex and dash:    2ed6657d-e927-468b-55e1-2665a8aea6a2-2dee3e35
Ver and Var Overwrite: xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
Final:                 2ed6657d-e927-568b-95e1-2665a8aea6a2
Discarded:                                                 -2dee3e35
~~~~
{: id='v5vervar' title='UUIDv5 Example Ver/Var bit swaps and discarded SHA-1 segment'}

## Example of a UUIDv6 Value {#uuidv6_example}

~~~~
-------------------------------------------
field       bits value
-------------------------------------------
time_high   32   0x1EC9414C
time_mid    16   0x232A
ver          4   0x6
time_high   12   0xB00
var          2   0b10
clock_seq   14   0b11, 0x3C8
node        48   0x9F6BDECED846
-------------------------------------------
total       128
-------------------------------------------
final: 1EC9414C-232A-6B00-B3C8-9E6BDECED846
~~~~
{: title='UUIDv6 Example Test Vector'}


## Example of a UUIDv7 Value {#uuidv7_example}

This example UUIDv7 test vector utilizes a well-known Unix epoch timestamp with
millisecond precision to fill the first 48 bits.

rand_a and rand_b are filled with random data.

The timestamp is Tuesday, February 22, 2022 2:22:22.00 PM GMT-05:00 represented
as 0x17F22E279B0 or 1645557742000


~~~~
-------------------------------------------
field       bits value
-------------------------------------------
unix_ts_ms  48   0x17F22E279B0
ver          4   0x7
rand_a      12   0xCC3
var          2   0b10
rand_b      62   0b01, 0x8C4DC0C0C07398F
-------------------------------------------
total       128
-------------------------------------------
final: 017F22E2-79B0-7CC3-98C4-DC0C0C07398F
~~~~
{: title='UUIDv7 Example Test Vector'}


## Example of a UUIDv8 Value (time-based) {#uuidv8_example}

This example UUIDv8 test vector utilizes a well-known 64 bit Unix epoch timestamp with
nanosecond precision, truncated to the least-significant, right-most, bits
to fill the first 48 bits through version.

The next two segments of custom_b and custom_c are filled with random
data.

Timestamp is Tuesday, February 22, 2022 2:22:22.000000 PM GMT-05:00 represented
as 0x16D6320C3D4DCC00 or 1645557742000000000

It should be noted that this example is just to illustrate one scenario for
UUIDv8. Test vectors will likely be implementation specific and vary greatly
from this simple example.


~~~~
-------------------------------------------
field     bits value
-------------------------------------------
custom_a  48   0x320C3D4DCC00
ver        4   0x8
custom_b  12   0x75B
var        2   0b10
custom_c  62   0b00, 0xEC932D5F69181C0
-------------------------------------------
total     128
-------------------------------------------
final: 320C3D4D-CC00-875B-8EC9-32D5F69181C0
~~~~
{: title='UUIDv8 Example Time-based Test Vector'}

## Example of a UUIDv8 Value (name-based) {#uuidv8_example_name}
A SHA-256 version of {{uuidv5_example}} is detailed in {{v8sha256}} to detail the usage of hashspaces {{hashspaces}} alongside namespaces {{namespaces}} and names.
The field mapping and all values are illustrated in {{v8fieldssha256}}.
Finally to further illustrate the bit swapping for version and variant and the unused/discarded part of the SHA-256 value see {{v8vervar}}.

~~~~
Hashspace (SHA2_256):  3fb32780-953c-4464-9cfd-e85dbbe9843d
Namespace (DNS):       6ba7b810-9dad-11d1-80b4-00c04fd430c8
Name:                  www.example.com
----------------------------------------------------------------
SHA-256:
401835fda627a70a073fed73f2bc5b2c2a8936385a38a9c133de0ca4af0dfaed
~~~~
{: id='v8sha256' title='UUIDv8 Example SHA256'}

~~~~
-------------------------------------------
field     bits value
-------------------------------------------
custom_a  48   0x401835fda627
ver        4   0x8
custom_b  12   0x70a
var        2   0b10
custom_c  62   0b00, 0x73fed73f2bc5b2c
-------------------------------------------
total     128
-------------------------------------------
final: 401835fd-a627-870a-873f-ed73f2bc5b2c
~~~~
{: id='v8fieldssha256' title='UUIDv8 Example Name-Based SHA-256 Test Vector'}

~~~~
A: 401835fd-a627-a70a-073f-ed73f2bc5b2c-2a8936385a38a9c133de0ca4af0dfaed
B: xxxxxxxx-xxxx-Mxxx-Nxxx-xxxxxxxxxxxx
C: 401835fd-a627-870a-873f-ed73f2bc5b2c
D:                                     -2a8936385a38a9c133de0ca4af0dfaed
~~~~
{: id='v8vervar' title='UUIDv8 Example Ver/Var bit swaps and discarded SHA-256 segment'}

Examining {{v8vervar}}:

{: spacing="compact"}

- Line A details the full SHA-256 as a hexadecimal value with the dashes inserted.
- Line B details the version and variant hexadecimal positions which must be overwritten.
- Line C details the final value after the ver/var have been overwritten.
- Line D details the discarded, leftover values from the original SHA-256 computation.
