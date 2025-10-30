# Black Duck SCA Samples                                                                                                                                                                                                                          

Live, executable samples using the Black Duck Security Scan Action with Black Duck SCA

## Table of Contents
- [Overview](#overview)
- [Workflows using Bridge CLI](#workflows-using-bridge-cli)
- [Workflows using Black Duck Security Scan Action](#workflows-using-black-duck-security-scan-action)
- [Helpful Links](#helpful-links)

## Overview

### What is Black Duck SCA? 

<details>
<summary><strong>📖 Click to learn when and why you need SCA scanning</strong></summary>

### 🔍 What SCA Detects:
- **Security Vulnerabilities:** Known CVEs in open source components with CVSS severity ratings
- **License Compliance Issues:** License conflicts and policy violations in dependencies
- **Outdated Components:** Libraries with available security patches or newer versions
- **Operational Risks:** End-of-life components and maintenance status

### ⏰ When Users Need SCA:
- **Pre-deployment:** Before releasing applications to production
- **Continuous Monitoring:** Ongoing scanning of existing applications
- **Dependency Updates:** When adding or updating third-party libraries
- **Compliance Audits:** During security assessments and regulatory reviews

### 👥 Critical User Scenarios:
- **Pull Request Validation:** Block PRs introducing vulnerable dependencies
- **Release Gate Controls:** Prevent deployment of applications with critical CVEs
- **Incident Response:** Rapid identification of affected components during security breaches
- **Vendor Assessments:** Generate security reports for customer requirements

### 💰 Business Impact:
- **Risk Reduction:** Prevent security breaches from vulnerable dependencies
- **Compliance Assurance:** Meet regulatory and contractual obligations
- **Cost Avoidance:** Avoid expensive post-deployment security fixes
- **Reputation Protection:** Maintain customer trust through proactive security

### 🚨 Key Triggers for SCA Implementation:
- **Customer security questionnaires** requiring vulnerability reports
- **Regulatory compliance mandates** (SOC 2, ISO 27001, GDPR)
- **Security incidents** involving third-party components
- **Merger & acquisition** due diligence requirements
- **Insurance requirements** for cyber liability coverage


</details>
                                                                                                                                                            

## Workflows using Bridge CLI
| How To? | Details | Workflow File | Scan Results |
|---------|---------|---------------|--------------|
| [**Scan repository with build as a pre-step (Recommended)**](https://github.com/blackducksca-workflow-samples/bridgecli) | This recommended method ensures SAST analysis on compiled code and artifacts through a pre-build step for comprehensive vulnerability detection | [Workflow](https://github.com/blackducksca-workflow-samples/bridgecli/blob/main/.github/workflows/BlackduckSCA_Bridge.yml) | [Results](https://blackducksca-workflow-samples.github.io/bridgecli/) ![Build Status](https://img.shields.io/github/actions/workflow/status/blackducksca-workflow-samples/bridgecli/BlackduckSCA_Bridge.yml) |

## Workflows using Bridge CLI
| How To? | Details | Workflow File | Scan Results | Build Statu |
|---------|---------|---------------|--------------|--------------|
| [**Scan repository with build as a pre-step (Recommended)**](https://github.com/blackducksca-workflow-samples/bridgecli) | This recommended method ensures SAST analysis on compiled code and artifacts through a pre-build step for comprehensive vulnerability detection | [Workflow](https://github.com/blackducksca-workflow-samples/bridgecli/blob/main/.github/workflows/BlackduckSCA_Bridge.yml) | [Results](https://blackducksca-workflow-samples.github.io/bridgecli/) | [![Build Status](https://img.shields.io/github/actions/workflow/status/blackducksca-workflow-samples/bridgecli/BlackduckSCA_Bridge.yml)](https://github.com/blackducksca-workflow-samples/bridgecli/actions) |

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
| [**Simplified workflow using default configurations for beginners**](https://github.com/blackducksca-workflow-samples/simplified-example) | Basic workflow demonstrating all Black Duck SCA features with default configurations. Ideal for beginners to explore features quickly. A perfect starting point to understand core capabilities without configuration complexity | [Workflow](https://github.com/blackducksca-workflow-samples/simplified-example/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/simplified-example/) | 
| [**Detailed workflow with full configurations for advanced users**](https://github.com/blackducksca-workflow-samples/detailed-example) | Comprehensive workflow demonstrating all Black Duck SCA capabilities with full configurations. Ideal for advanced users requiring granular control and customization capabilities | [Workflow](https://github.com/blackducksca-workflow-samples/detailed-example/blob/main/.github/workflows/nodejs-npm.yml) | [Results](https://blackducksca-workflow-samples.github.io/detailed-example/) | 


## Helpful Links                                                                                                                                                                                                                         
[Using the Black Duck Security Scan Action with Black Duck SCA Documentation](https://documentation.blackduck.com/bundle/bridge/page/documentation/c_github-blackduck.html)
