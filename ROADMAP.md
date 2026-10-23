<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
SPIKE-CALIBRATOR — repository governance and provenance
-->

# Roadmap

Implemented local tooling validates repository metadata, source, workflows, development dependencies, documentation and inventory through fixed command surfaces. It does not evaluate model confidence or qualify calibration evidence.

Planned classifier evaluation binds actual model/data/labels, raw spiking output, class order, ties, censoring and an explicit source-defined confidence mapping. Spike count, first-spike time and population agreement do not by themselves define probabilities. Proper scoring requires a supported categorical probability vector; confidence-only output cannot acquire one implicitly.

Planned metrics retain complete bins and samples, explicit boundary conventions, finite ECE/MCE and unnormalized categorical Brier. Natural-log NLL needs a bound method and normalization, a qualified numerical enclosure, and explicit unavailability at true-class probability zero. Empty bins and unavailable data cannot become a zero score. Finite descriptions do not establish future-population confidence.

The whole declared shift-by-level-by-placement-by-trial population includes baseline, noise, amplitude, temporal warp and sensor drift with their actual transforms, units and source/label validity. Placement drift requires compatible actual reports. Software evaluation stands alone; fabric claims require genuine accepted physical evidence.

The intended public operations are evaluate, shift, drift, report, gate and verify. They are not installed here. V1 measures confidence and applies prior thresholds; it does not fit post-hoc corrections, develop new uncertainty estimators, calibrate meters or fit physical substrate parameters.

Completion requires the full owned report contract, independent scoring and miscalibration cases, real model/data and separate consumer integration, strict native checks, meaningful coverage, documentation and fresh comparison benchmarks for implemented counterparts. Unknown required curves, quality or policy outcomes cannot authorize deployment.
