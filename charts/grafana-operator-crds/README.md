# grafana-operator-crds

Helper chart to add as a dependency for grafana-operator
Should materialize dashboards and grafana instances

Use as follows:

* In main chart add it as dependency
```
dependencies:
  - name: grafana-operator
    version: "v5.15.1"
    repository: "oci://ghcr.io/grafana/helm-charts"
  - name: grafana-operator-crds
    version: ""
    repository:
```

* Add additional to values.yaml configurations files

    * dashboard-values.yaml - list of dashboards
    * grafana-values.yaml - list of grafana instances

* Helm chart should render
* Point DWAT to dashboard-values.yaml