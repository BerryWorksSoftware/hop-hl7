# BerryWorks HL7 Input 0.2.0-rc1

First release candidate of the separate BerryWorks HL7 Input plugin for Apache Hop.
This is preview software for evaluation, not a production clinical integration.

## Requirements

- Apache Hop 2.19.0
- Java 21 or later

## Install

1. Download `hop-hl7-plugin-0.2.0-rc1.zip` and its `.sha256` file from this release.
2. Verify the ZIP checksum. On macOS/Linux, run `shasum -a 256 -c hop-hl7-plugin-0.2.0-rc1.zip.sha256` in the download folder.
3. Stop Hop. If replacing an HL7 candidate, remove the old `plugins/transforms/hop-hl7-plugin/` folder first.
4. Extract the ZIP into the Hop installation root, where `hop-gui.sh` or `hop-gui.bat` resides.
5. Restart Hop and find **HL7 Input** under **BerryWorks HL7**.

The EDI plugin may remain installed. HL7 Input uses its own transform ID,
`BerryWorksHl7Input`, and installation folder.

## Try the admission Quick Start

Follow the [HL7 admission Quick Start](https://github.com/BerryWorksSoftware/hop-hl7/tree/v0.2.0-rc1/quick-start-hl7).
It includes a synthetic ADT_A01/2.5.1 admission message, a YAML model, a pipeline,
and expected CSV results: two procedures and two insurance plans, plus 30 parser rows.

## Scope and verification

The candidate bundles an ADT_A01/2.5.1 model. ORU loop detection, full HL7
compliance validation, and production clinical mappings are outside its scope.

All 28 active regression tests passed against the processed plugin and obfuscated
runtime. Isolated command-line runs matched both expected CSVs, including a run
using the bundled model. Manual Hop 2.19.0 testing verified discovery alongside
EDI Input, configuration dialog labels, and matching Quick Start outputs.

The package includes the unchanged public EDIReader parser, an obfuscated
proprietary BerryWorks framework runtime, and SnakeYAML. Component notices and
license terms are included in the ZIP.

Report feedback through [GitHub Issues](https://github.com/BerryWorksSoftware/hop-hl7/issues)
using synthetic examples without patient data.
