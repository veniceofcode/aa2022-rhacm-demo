# Demonstrate placement algorithm
## Tool Requirements
- OpenShift CLI Version >= 4.3.0<br>_Needed for kustomize_
```bash
oc version
```

## This example, allows you to demonstrate using an Ansible Pre & Post job.
1. Add the subscription to your Red Hat Advanced Cluster Management for Kubernetes HUB
```
clone https://github.com/veniceofcode/aa2022-rhacm-demo.git
oc apply -k aa2022-rhacm-demo/tree/main/demo/rhacm/subscription/
```
### Using
- Navigate to the Manage applications in the UI. Click the `nginx-ansible-demo` Application name.
- View the Topology, look around, by default the application should have deployed to `vendor: OpenShift` clusters
- Make adjustments directly in the Topology
```yaml
  clusterSelector:
    matchLabels: {}
```
