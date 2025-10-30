# Black Duck SCA Samples                                                                                                                                                                                                                          

Live, executable samples using the Black Duck Security Scan Action with Black Duck SCA

## Table of Contents
- [Overview](#overview)
- [Workflows using Bridge CLI](#workflows-using-bridge-cli)
- [Workflows using Black Duck Security Scan Action](#workflows-using-black-duck-security-scan-action)
- [Helpful Links](#helpful-links)

## Overview

## What is Black Duck SCA? 

<details>
<summary><strong>📖 Click to learn when and why you need SCA scanning</strong></summary>

### 🔍 What SCA Detects:
- **Security Vulnerabilities:** Known CVEs with CVSS scores, exploit availability, and remediation paths
- **License Risks:** GPL conflicts, commercial restrictions, attribution requirements, copyleft obligations
- **Supply Chain Threats:** Malicious packages, typosquatting attacks, compromised dependencies
- **Technical Debt:** Outdated libraries, end-of-life components, unmaintained projects

### ⏰ When Users Need SCA:
- **Pre-Commit:** Developer workstation scanning before code submission
- **CI/CD Pipeline:** Automated build validation and release gate enforcement  
- **Production Monitoring:** Continuous vulnerability tracking and new CVE alerting
- **Compliance Events:** Audit preparation, customer security reviews, regulatory reporting

### 👥 Critical User Scenarios:
- **Developers:** *"Is this dependency secure?"* → Instant vulnerability and license validation
- **Security Teams:** *"Are we affected by the latest CVE?"* → Rapid impact assessment across all applications
- **Legal Teams:** *"Can we distribute this commercially?"* → License compliance verification and risk analysis
- **DevOps Teams:** *"Should we block this deployment?"* → Risk-based release decisions with clear thresholds

### 💰 Business Impact:
- **Risk Mitigation:** 96% of applications contain open source code; 84% have known vulnerabilities *(Synopsys OSSRA 2024)*
- **Cost Avoidance:** Average security breach costs $4.88M; prevention costs significantly less *(IBM Security 2024)*
- **Compliance Assurance:** Automated license tracking prevents legal disputes and contract violations
- **Developer Velocity:** Early detection reduces fixing costs by 100x compared to production remediation

### 🚨 Key Triggers for SCA Implementation:
- **Security Incidents:** Vulnerability exploits in your technology stack
- **Compliance Requirements:** SOX, GDPR, HIPAA mandating software inventory
- **Customer Demands:** Enterprise buyers requiring security attestations
- **Supply Chain Attacks:** SolarWinds-style incidents highlighting third-party risks
- **Developer Productivity:** Reducing time spent on manual security research

**Bottom Line:** SCA is essential for any organization using open source components (99% of modern applications) to manage security, legal, and operational risks effectively.

</details>

## Workflows using Bridge CLI
| How To? | Details | Workflow File | Scan Results |                                                                                                                                                                
|---------|-------------|---------------|---------------------|                                                                                                                                                               
| [**Scan repository with build as a pre-step (Recommended)**](https://github.com/blackducksca-workflow-samples/full-scan) | This recommended method ensures SAST analysis on compiled code and artifacts through a pre-build step for comprehensive vulnerability detection | [Workflow](https://github.com/blackducksca-workflow-samples/full-scan/blob/main/.github/workflows/nodejs-npm.yml) |[Results](https://blackducksca-workflow-samples.github.io/full-scan/) |


## Workflows using Black Duck Security Scan Action

| How To? | Details | Workflow File | Scan Results |                                                                                                                                                                
|---------|-------------|---------------|---------------------|                                                                                                                                                               
| [**Scan repository with build as a pre-step (Recommended)**](https://github.com/blackducksca-workflow-samples/full-scan) | This recommended method ensures SAST analysis on compiled code and artifacts through a pre-build step for comprehensive vulnerability detection | [Workflow](https://github.com/blackducksca-workflow-samples/full-scan/blob/main/.github/workflows/nodejs-npm.yml) |[Results](https://blackducksca-workflow-samples.github.io/full-scan/) |
| [**Scan repository in an environment where build is not an option**](https://github.com/blackducksca-workflow-samples/buildless-scan) | This option is less accurate and should be used when you can't build your repository | [Workflow](https://github.com/blackducksca-workflow-samples/buildless-scan/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/buildless-scan/) |
| [**PR Comments**](https://github.com/blackducksca-workflow-samples/pr-comments) | For each new vulnerable component that the developer introduces with his/her changes, this integration is capable of adding a comment to the pull request. PR comments enable the developer to quickly view, understand and fix the issue before merging the pull request | [Workflow](https://github.com/blackducksca-workflow-samples/pr-comments/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/pr-comments/) |                                                                                     
| [**Create Automatic FixPRs**](https://github.com/blackducksca-workflow-samples/automatic-fixpr) | Fix PR feature automatically creates PRs for vulnerable components found in the scan. This sample shows how you can configure the fix PR feature | [Workflow](https://github.com/blackducksca-workflow-samples/automatic-fixpr/blob/main/.github/workflows/automatic-fixpr.yml) | [Results](https://blackducksca-workflow-samples.github.io/automatic-fixpr/) |                                                                            
| [**Generate Sarif Reports**](https://github.com/blackducksca-workflow-samples/sarif-generation) | This sample shows how you can create a SARIF file for SCA issues found in the scan | [Workflow](https://github.com/blackducksca-workflow-samples/sarif-generation/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/sarif-generation/) |                                                                          
| [**Import issues into GitHub Advanced Security**](https://github.com/blackducksca-workflow-samples/sarif-generation) | This sample shows how you can post SCA issues found in the scan to Code Scanning tab in GitHub Advanced Security | [Workflow](https://github.com/blackducksca-workflow-samples/sarif-generation/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/sarif-generation/) |
| [**Build Break**](https://github.com/blackducksca-workflow-samples/build-break) | The ability to break or not break a build when policy violations are found is configurable. This sample shows you how to configure the build break options |  [Workflow](https://github.com/blackducksca-workflow-samples/build-break/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/build-break/) |                                                                                    
| [**Passing Detect tool arguments from Black Duck Sca scans**](https://github.com/blackducksca-workflow-samples/arbitrary-params) | To leverage advanced SCA features, you need to pass options to Detect. This sample shows how you can configure Detect options |  [Workflow](https://github.com/blackducksca-workflow-samples/arbitrary-params/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/arbitrary-params/) |                                                                           
| [**Run scans asynchronously to avoid holding up the pipeline during scanning**](https://github.com/blackducksca-workflow-samples/async-mode) | By default, the pipeline is held until the scan finishes. You can configure the workflow in such a way where the pipeline doesn't wait for the scan to finish and returns immediately after kicking off the scan. Note that post scan options are not triggered when you choose to not wait for the scan to finish | [Workflow](https://github.com/blackducksca-workflow-samples/async-mode/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/async-mode/) |  


## Helpful Links                                                                                                                                                                                                                         
[Using the Black Duck Security Scan Action with Black Duck SCA Documentation](https://documentation.blackduck.com/bundle/bridge/page/documentation/c_github-blackduck.html)
