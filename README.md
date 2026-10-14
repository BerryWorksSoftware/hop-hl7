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

## Quick Start

Explore the [HL7 admission Quick Start](quick-start-hl7/README.md), which includes
an entirely synthetic `ADT^A01` message, a YAML model, a Hop pipeline, and expected
CSV results for procedures and insurance plans. Running it currently requires an
unreleased development build with HL7 support; the example is available for
inspection ahead of the first public preview.

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
