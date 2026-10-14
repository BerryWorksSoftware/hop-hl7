# BerryWorks HL7 Plugin for Apache Hop

HL7 v2 integration plugin for Apache Hop, powered by the BerryWorks EDIReader
Framework.

## Development status

This plugin is under development. No HL7 plugin release or installation package
is available from this repository yet. Installation instructions and supported
Hop and Java versions will be published with the first preview release.

The initial direction is to read HL7 v2 messages into structured rows for use in
Hop pipelines. An admission notification (`ADT^A01`) is the first demonstration
target, including patient context, procedures, and insurance groups.

## About this repository

This is the public home for the plugin's documentation, examples, release
information, and downloads as they become available. Development source is
maintained separately in the shared BerryWorks Hop plugin codebase.

The HL7 plugin and the [BerryWorks EDI plugin for Apache Hop](https://github.com/BerryWorksSoftware/hop-edi)
have separate public identities and share underlying BerryWorks technology.
The EDI plugin's existing 0.1.0 preview does not include HL7 support.

## Feedback

Use this repository's [issue tracker](https://github.com/BerryWorksSoftware/hop-hl7/issues)
for questions, feature requests, and feedback. For parsing issues, include the
message type and HL7 version, relevant error details, and a small synthetic
example. Do not include patient information or other sensitive data.
