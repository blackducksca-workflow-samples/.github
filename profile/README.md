# Black Duck SCA Workflow Samples                                                                                                                                                                                                                
                                                                                                                                                                                                                                         
Live, executable examples demonstrating Black Duck SCA integration with CI/CD pipelines.                                                                                                                                                                                                                                                                                                                                                                  
## Quick Start                                                                                                                                                                                                                                                                                                                                                                                                                                            
1. Choose a Workflow Sample from the table above                                                                                                                                                                                                 
2. Click the workflow file to see the configuration                                                                                                                                                                                      
3. Click the latest scan results to see latest scan execution                          

## Workflows                                                                                                                                                                                                                  
                                                                                                                                                                                                                                         
| Workflow Samples | Details | Workflow File | Scan Results |                                                                                                                                                                          
|---------|-------------|---------------|---------------------|                                                                                                                                                                          
| **Branch Scans (Build Method)** | Run Black Duck SCA scan by building the project source code | [→ View Workflow](https://github.com/blackducksca-workflow-examples/full-scan/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/full-scan/) |

| **Branch Scans (Buildless Method)** | Black Duck Sca scan without building the project | [→ View Workflow](https://github.com/blackducksca-workflow-examples/install-directory-custom-paths/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/install-directory-custom-paths/) |


| **PR Comments** | Automated security feedback on pull requests | [→ View Workflow](https://github.com/blackducksca-workflow-examples/pr-comments/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/pr-comments/) |

| **Automatic FixPR** | Automated fix pull request creation | [→ View Workflow](https://github.com/blackducksca-workflow-examples/automatic-fixpr/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/automatic-fixpr/) |

| **SARIF Generation** | Security report generation in SARIF format | [→ View Workflow](https://github.com/blackducksca-workflow-examples/sarif-generation/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/sarif-generation/) |

| **Build Break** | Fail builds on security policy violations | [→ View Workflow](https://github.com/blackducksca-workflow-examples/build-break/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/build-break/) |

| **Arbitrary Params** | Custom parameter configurations | [→ View Workflow](https://github.com/blackducksca-workflow-examples/arbitrary-params/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/arbitrary-params/) |

| **Async Mode** | Asynchronous scanning mode | [→ View Workflow](https://github.com/blackducksca-workflow-examples/async-mode/blob/main/.github/workflows/nodejs-npm.yml) | [→ View Results](https://blackducksca-workflow-examples.github.io/async-mode/) |
                                                                                                                                                                                                                                                                                                                                                                                                 
## Documentation                                                                                                                                                                                                                         
For detailed configuration options, visit the [Black Duck GitHub Integration Documentation](https://documentation.blackduck.com/bundle/bridge/page/documentation/c_github-blackduck.html). 
