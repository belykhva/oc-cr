
c-cr
Simple oc plugin for getting all CustomResources within Kubernetes/Openshift project

# Installation
```
# git clone https://github.com/belykhva/oc-cr.git
# cp ./oc-cr/oc-cr /usr/local/bin
# chmod +x /usr/local/bin/oc-cr
```
# Using
Test plugin enabling:
```
# oc plugin list

[root@localhost]# oc plugin list
The following compatible plugins are available:
...
/usr/local/bin/oc-cr
...
```
Show current project:
```
[root@localhost]# oc project
Using project "openshift-kube-apiserver" on server "https://api.ocp.domain.com:6443".
```
Get all CustomResources in current project:
```
[root@localhost]# oc cr

NAME                                                                             DISPLAY                        VERSION   REPLACES   PHASE
clusterserviceversion.operators.coreos.com/openshift-pipelines-operator.v0.5.2   OpenShift Pipelines Operator   0.5.2                Succeeded
NAME                                           AGE
servicemonitor.monitoring.coreos.com/monitor   4d2h
```
# TO-DO
- Add namespace selection support
- Add bash-completion support for namespaces
