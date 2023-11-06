# Red Hat Helm Charts
This repository contains the charts are populated out-of-the-box in the OpenShift Developer Catalog

The repository has been configured to serve the static helm index and chart files

## Usage

```

$ helm repo add redhat-charts https://redhat-developer.github.io/redhat-helm-charts
"redhat-charts" has been added to your repositories

$ helm repo list 
NAME           	URL                               
redhat-charts	https://redhat-developer.github.io/redhat-helm-charts  

```


## Helm index

https://redhat-developer.github.io/redhat-helm-charts/index.yaml
 

## [How To Submit a New Chart](https://github.com/redhat-developer/redhat-helm-charts/wiki/Adding-a-New-Chart)


Vendor:

    Meterian Scanner: Meterian is a commercial product offered by Meterian Ltd.
    Nexus IQ Scanner: Nexus IQ is a product of Sonatype, a well-established company in the DevSecOps and software supply chain management space.

Purpose:

    Meterian Scanner: Meterian focuses on identifying and mitigating open-source software vulnerabilities in your applications and containers.
    Nexus IQ Scanner: Nexus IQ is a more comprehensive solution that not only identifies vulnerabilities in open-source components but also helps with policy enforcement, license compliance, and application composition analysis.

Vulnerability Scanning:

    Meterian Scanner: It scans for vulnerabilities in open-source components used in your software applications.
    Nexus IQ Scanner: It also scans for vulnerabilities but goes beyond by providing detailed information about the components, their licenses, and allowing you to set and enforce policies for their usage.

Policy Enforcement:

    Meterian Scanner: It has basic policy checks, but it's not as robust as Nexus IQ in terms of policy enforcement and customization.

License Compliance:

    Meterian Scanner: It may provide some basic information about open-source licenses but doesn't have the depth and flexibility of Nexus IQ in terms of license compliance checks.

Integration and Ecosystem:

    Meterian Scanner: It may have integrations with various development tools and CI/CD pipelines but might not be as extensive as the Nexus IQ ecosystem.

Customization:

    Meterian Scanner: Provides some level of customization, but it's more limited compared to Nexus IQ, which allows for extensive rule and policy customization.

Community and Support:

    Meterian Scanner: Support and community resources might not be as extensive as those available for Nexus IQ due to the difference in company size and product maturity.

Scalability:

    Meterian Scanner: Suitable for smaller to mid-sized organizations.
    Nexus IQ Scanner: More suitable for larger enterprises with complex software supply chain management needs.

Cost:

    The cost of both tools may vary based on the features and usage. Nexus IQ is known to be on the higher end in terms of pricing due to its feature set.

    stage('input') {
                    steps {
                        script {
                            node( 'master') {
                                def inputFile = input message: 'Upload Artifact', parameters: [file(name: 'upload_file')]
                                def uploadFile = inputFile.remote
                                sh "cp ${uploadFile} ${LOCAL_PATH}"
                                stash name: 'upload-artifact', includes: "${LOCAL_PATH}"
                            }    
                        }
                    }
                }
