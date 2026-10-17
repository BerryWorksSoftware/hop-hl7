# HL7 Input 0.2.0-rc1

Release candidate uploaded to a GitHub draft; not yet publicly released or available through Marketplace.

## Candidate identity

- Transform: **HL7 Input**, category **BerryWorks HL7**.
- Transform ID: `BerryWorksHl7Input`.
- Package: `hop-hl7-plugin-0.2.0-rc1.zip`, with a separate SHA-256 file.
- Installation folder: `plugins/transforms/hop-hl7-plugin/`.
- Target: Apache Hop 2.19.0, Java 21.
- Bundled model: ADT_A01, HL7 2.5.1.

## Validation completed

- 28 active regression tests passed against the processed plugin and obfuscated
  framework; the existing ORU loop test is skipped and ORU is outside scope.
- SHA-256 and ZIP integrity checked; private mappings and tests excluded.
- The public Quick Start ran in an isolated Hop 2.19.0 command-line environment
  without the installed EDI/development plugins.
- Both generated CSVs matched the supplied expected results: four admission-item
  rows and 30 parser rows.
- The same comparison passed using the model extracted from the candidate ZIP.

## GUI validation completed

Manual testing in Hop 2.19.0 confirmed discovery alongside EDI Input, the
HL7 Input configuration dialog with HL7 labels, and successful Quick Start
execution. Both freshly generated CSVs matched the expected files.

## Before publishing

- Commit and push the updated README, complete Quick Start (including its pipeline
  and output/.gitkeep), release notes, and Marketplace metadata.
- Set the release tag `v0.2.0-rc1` to that commit, not the older repository state.
- Review the draft release and the two attached assets: ZIP and checksum only.
- Publish as a **pre-release** when approved.
- Test anonymous download, checksum, installation, and the tagged Quick Start.
- Then import the Marketplace repository definition and test its installation.
  Draft release assets are not anonymously downloadable, so that test requires
  the pre-release to be public.

The candidate demonstrates synthetic admission parsing, not full HL7 compliance
validation or production clinical mappings. See the [Quick Start scope](quick-start-hl7/README.md#scope-of-this-example).

## GitHub draft

[Review the saved draft](https://github.com/BerryWorksSoftware/hop-hl7/releases/edit/untagged-bcaeb4b490cb9e48a55e).
The ZIP and checksum are attached. GitHub's displayed SHA-256 digests match
both local files. The intended tag is `v0.2.0-rc1`, created only on publication.
Update main with the prepared public files before publishing the draft.
The Marketplace definitions passed YAML and matching-entry checks locally;
their rendered release download URL matches the candidate asset name.
