<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SPIKE-CALIBRATOR — repository governance and provenance
-->

# Validation tooling API

The metadata command accepts `--root` and `--json`. The inventory command additionally accepts `--mode generate|verify` and requires `--output` only for generation. All commands emit safe structured JSON. Exits are 0 for the requested scope, 2 for refusal, 3 for unavailable required inputs or tools, and 4 for invalid invocation or configuration.

Metadata validation accepts no generated inventory dependency. Inventory generation publishes deterministic new bytes; verification requires the canonical inventory and complete initial paths. A successful operation does not qualify confidence mappings, score correctness or deployment outcomes or establish release readiness.

## Metadata acceptance

::: calibrator_validation.metadata.validate_metadata

## Finite input

::: calibrator_validation.inputs.read_file

::: calibrator_validation.inputs.read_json

## Capability inventory

::: calibrator_validation.capabilities.inventory_bytes

::: calibrator_validation.capabilities.create_inventory

::: calibrator_validation.capabilities.validate_capabilities

## Diagnostics

::: calibrator_validation.report.Finding

::: calibrator_validation.report.Report

## Command interfaces

::: calibrator_validation.cli.metadata_main

::: calibrator_validation.cli.inventory_main

## Source ownership and maintained tree

::: calibrator_validation.provenance.validate_notice

::: calibrator_validation.provenance.validate_provenance

::: calibrator_validation.structure.maintained_paths

::: calibrator_validation.structure.validate_structure

## YAML and workflow policy

::: calibrator_validation.yaml_input.read_yaml

::: calibrator_validation.workflows.validate_workflows

## Complete dependency observations

Release candidates and observed installed metadata are separate records. The hash lock covers the entire selected development graph. Exact source-builder constraints also use that lock. Recorded installation RECORD hashes are observations; relocated entry-script paths prevent treating them as universal build identities. Custom licence references retain exact source terms and do not infer permissions.

::: calibrator_validation.dependency_lock.parse_direct

::: calibrator_validation.dependency_lock.parse_lock

::: calibrator_validation.dependency_records.Artifact

::: calibrator_validation.dependency_records.LicenseEvidence

::: calibrator_validation.dependency_records.LicenseSource

::: calibrator_validation.dependency_records.PackageRecord

::: calibrator_validation.dependency_records.read_provenance

::: calibrator_validation.dependencies.verify_records

::: calibrator_validation.dependencies.verify_installed

::: calibrator_validation.dependencies.verify_configuration

::: calibrator_validation.dependencies.validate_dependencies

::: calibrator_validation.native_tools.verify_native_tools

## Actual documentation rendering

::: calibrator_validation.documentation.References

::: calibrator_validation.documentation.render_markdown

::: calibrator_validation.documentation.inspect_markdown

::: calibrator_validation.documentation.build_site

::: calibrator_validation.documentation.inspect_projection

::: calibrator_validation.documentation.validate_documentation

## Tool completion and scoped preflight

Every tool uses a fixed absolute executable, literal arguments and a finite deadline. Actual exits survive communication errors where observed. Output limits apply to accepted completed output; the caller reserves process memory separately. A named preflight subset reports its narrower scope. The complete operation requires the entire compiled profile. Missing tools, invalid protocol and native failures retain their real states.

::: calibrator_validation.execution.ToolResult

::: calibrator_validation.execution.run_tool

::: calibrator_validation.preflight.Check

::: calibrator_validation.preflight.Outcome

::: calibrator_validation.preflight.PreflightReport

::: calibrator_validation.preflight.validate_checker_report

::: calibrator_validation.preflight.run_check

::: calibrator_validation.preflight.run_checks

::: calibrator_validation.preflight.source_payload

::: calibrator_validation.validation_profile.scaffold_checks

::: calibrator_validation.preflight_cli.preflight_main

## Shared command and protocol interfaces

::: calibrator_validation.inputs.parse_json

::: calibrator_validation.report.Refusal

::: calibrator_validation.cli.Parser

::: calibrator_validation.cli.check_main

::: calibrator_validation.cli.emit_report

::: calibrator_validation.ci_dependencies.verify_ci_dependencies

## Native workflow composition

The coordinator executes the eight complete native jobs from the maintained workflow sources. Each of four category gates requires every actual descendant result, and the stable required gate checks all four category results. The workflow policy verifies exact job equality with each source and rejects missing descendants, masked outcomes, altered commands and workflow calls. This preserves all category checks without depending on an unsupported reusable-workflow syntax. Both native syntax and unchanged pedantic workflow checks inspect the actual executable configuration; no projected input or suppressed finding is used.
