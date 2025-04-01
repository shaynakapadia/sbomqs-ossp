<!--
 Copyright 2023 Interlynk.io

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->

# `sbomqs-ossp`: Quality metrics for SBOMs adapted for OSSP

Code forked from https://github.com/interlynk-io/sbomqs for use with LLNL-OSSP

# Scoring Criteria
1. Components have names (accounting for placeholders)
2. Components have valid spdx licenses
3. Components contain version information (accounting for placeholders)
4. Components have Supplier and/or Author information (accounting for placeholders)
5. Components contain at least one valid purl or cpe 
6. Components contain at least one dependency

# Usage
To calculate the OSSP specific score, run:
`go build -o sbomqs-ossp main.go`
`./sbomqs-ossp score <PATH-TO-SBOM> --configpath features.yaml`