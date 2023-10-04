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



=SUBSTITUTE(A1, LEFT(A1, FIND("~", SUBSTITUTE(A1, ".", "~", LEN(A1)-LEN(SUBSTITUTE(A1, ".", "")) - 1))-1), REPT("*", LEN(LEFT(A1, FIND("~", SUBSTITUTE(A1, ".", "~", LEN(A1)-LEN(SUBSTITUTE(A1, ".", "")) - 1))-1))))


