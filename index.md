<p align="center">
  <a href="https://helm.sh"><img src="https://helm.sh/img/helm.svg" alt="Helm logo" title="Helm" height="90"/></a>&nbsp;
</p>

# Install Helm Repository

The `vsphere-cpi-csi` Chart can be installed from [https://sphr2k.github.io/vsphere-cpi-csi/](http://docs.wildfly.org/wildfly-charts/)

```
$ helm repo add vsphere-cpi-csi https://sphr2k.github.io/vsphere-cpi-csi/
"vsphere-cpi-csi" has been added to your repositories

$ helm repo update
...Successfully got an update from the "vsphere-cpi-csi" chart repository

$ helm search repo vsphere-cpi-csi --versions
NAME                            CHART VERSION   APP VERSION     DESCRIPTION
vsphere-cpi-csi/vsphere-cpi-csi 2.2.1           2.2.1           vSphere CPI manager and CSI drivers
vsphere-cpi-csi/vsphere-cpi-csi 2.1.0           2.1.0           vSphere CPI manager and CSI drivers
````

# Install vSphere CPI+CSI Chart

Install with minimum parameters required:

```
$ helm install vsphere-cpi-csi/vsphere-cpi-csi \
     --namespace kube-system \
     ./charts/vsphere-cpi-csi/v2.2.1 \
     --set vcenter.host=vsphere.example.com \
     --set vcenter.username=johndoe \
     --set vcenter.password=s3cret \
     --set vcenter.datacenter=dc1
```

# Documentation

A more complete documentation can be found in the [[GitHub repo]](https://github.com/sphr2k/vsphere-cpi-csi).
