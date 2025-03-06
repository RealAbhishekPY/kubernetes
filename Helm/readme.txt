Helm is a package manager for Kubernetes that allows you to define, install, and upgrade even the most complex Kubernetes applications. A Helm chart is a collection of files that describe a related set of Kubernetes resources.

mychart
|-- Chart.yaml
|-- charts
|-- templates
|   |-- NOTES.txt
|   |-- _helpers.tpl
|   |-- deployment.yaml
|   |-- ingress.yaml
|   `-- service.yaml
`-- values.yaml

### Explanation:
- **Chart.yaml**: Contains metadata about the chart, such as its name, version, and description.
- **values.yaml**: Defines default values for the chart's variables, which can be overridden during installation.
- **templates/**: Contains Kubernetes resource templates that use the values defined in `values.yaml`.

This example creates a simple Helm chart for deploying an Nginx application with a Deployment and a Service. The templates use placeholders (e.g., `{{ .Values.replicaCount }}`) to inject values from `values.yaml`.

