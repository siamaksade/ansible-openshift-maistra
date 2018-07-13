Ansible Role: Istio and Jaeger on OpenShift
[![Build Status](https://travis-ci.org/siamaksade/ansible-openshift-istio.svg?branch=master)](https://travis-ci.org/siamaksade/ansible-openshift-istio)
=========

Ansible Role for deploying Istio service mesh and Jaeger on OpenShift


Role Variables
------------

|Variable                  | Default Value            | Description   |
|--------------------------|--------------------------|---------------|
|`istio_version`           | 0.8.0               | Istio version to deploy |
|`openshift_master_public` | -                        | OpenShift master public url (required) |
|`enable_istio_auth`       | `false`                  | Enable Istio mTLS authentication |
|`kiali_username`              | `admin`                  | Kiali username |
|`kiali_password`          | `admin`                  | Kiali password |
|`openshift_cli`           | oc                       | OpenShift CLI command and arguments (e.g. auth)       | 


Example Playbook
------------

```
name: Example Playbook
hosts: localhost
tasks:
- import_role:
    name: siamaksade.openshift_istio
  vars:
    openshift_master_public: https://master.openshift.mydomain.com
```