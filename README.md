# helm
- A package manager for kubernetes applications
- Templatise the manifest files(reusable)

***Installations:***
```
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4
chmod 700 get_helm.sh
  ./get_helm.sh

helm version
```
***Deployment Steps:***
- Add repo => helm repo add aws-ebs-csi-driver https://kubernetes-sigs.github.io/aws-ebs-csi-driver
- help repo update
- Install the packages(set of kube resources) =>

***Charts:***
```
Chart.yaml          # A YAML file containing information about the chart
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart
  README.md           # OPTIONAL: A human-readable README file
  values.yaml         # The default configuration values for this chart
  values.schema.json  # OPTIONAL: A JSON Schema for imposing a structure on the values.yaml file
  charts/             # A directory containing any charts upon which this chart depends.
  crds/               # Custom Resource Definitions
  templates/          # A directory of templates that, when combined with values,
                      # will generate valid Kubernetes manifest files.
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes
apiVersion: The chart API version (required)
name: The name of the chart (required)
version: The version of the chart (required)
kubeVersion: A SemVer range of compatible Kubernetes versions (optional)
description: A single-sentence description of this project (optional)
```

1. Steps
   - Inside helm folder create a Chart.yaml file (first letter should be upper case).
   - Add apiVersion, name of the chart, version of the chart, there parameters are mandatory
   - 
