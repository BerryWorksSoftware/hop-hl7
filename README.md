# BerryWorks HL7 Plugin for Apache Hop

HL7 v2 integration plugin for Apache Hop, powered by the BerryWorks EDIReader
Framework.

## Development status

This plugin is under development. Release candidate **0.2.0-rc1** is being
validated locally with **Apache Hop 2.19.0** and **Java 21**. No public GitHub
release or Marketplace installation is available yet.

The initial direction is to read HL7 v2 messages into structured rows for use in
Hop pipelines. An admission notification (`ADT^A01`) is the first demonstration
target, including patient context, procedures, and insurance groups.

## Quick Start

Explore the [HL7 admission Quick Start](quick-start-hl7/README.md), which includes
an entirely synthetic `ADT^A01` message, a YAML model, a Hop pipeline, and expected
CSV results for procedures and insurance plans. Running it requires the separate HL7 Input
release candidate described below.

## Install the release candidate

These steps apply when you have been given `hop-hl7-plugin-0.2.0-rc1.zip` and
its `.sha256` checksum file for testing.

1. Verify the ZIP against the supplied SHA-256 checksum.
2. Stop Hop GUI and other Hop processes using the installation.
3. If replacing an earlier HL7 candidate, remove its
   `plugins/transforms/hop-hl7-plugin/` folder before extraction.
4. Extract the ZIP into the **Hop installation root**, the folder containing
   `hop-gui.sh` or `hop-gui.bat`. It creates `plugins/transforms/hop-hl7-plugin/`.
5. Restart Hop. Find **HL7 Input** under **BerryWorks HL7**.
6. Run the [admission Quick Start](quick-start-hl7/README.md) and compare its
   two output CSVs with the files in its `expected` folder.

The EDI plugin may remain installed: the HL7 transform has a separate ID and
installation folder. The candidate bundles an ADT_A01/2.5.1 YAML model under
`plugins/transforms/hop-hl7-plugin/models/`. The Quick Start uses its own copy.

## Preview scope

The first candidate demonstrates parsing synthetic ADT_A01 admissions, including
procedure and insurance groups, into structural and business rows. It does not
provide full HL7 compliance validation or clinically validated patient mappings.
ORU loop detection is outside this candidate's supported scope.

The package includes the unchanged public BerryWorks EDIReader parser, a reduced
and obfuscated proprietary BerryWorks framework runtime, and SnakeYAML. See the
bundled `NOTICE.txt` and `licenses/` directory for component terms.

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
