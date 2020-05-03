# cwmtoolbox

CWM Platform 3rd Party Tools Integration

## Apache Libcloud

[Libcloud](https://libcloud.readthedocs.io/en/latest/) is a Python library for interacting with many of the popular cloud service providers using a unified API.

CWM Platform is supported in the latest development version and will be available starting from version 3.0.0

Documentation:

* [Installation of the development version](https://libcloud.readthedocs.io/en/latest/getting_started.html#installation-development-version)
* [Kamatera compute driver](https://libcloud.readthedocs.io/en/latest/compute/drivers/kamatera.html)

## Ansible

[Ansible](https://docs.ansible.com/ansible/latest/user_guide/) delivers simple IT automation that ends repetitive tasks and frees up DevOps teams for more strategic work.

The Kamatera collection can be installed using Ansible version 2.9 with the following command:

```
ansible-galaxy collection install https://github.com/OriHoch/ansible-collection-kamatera/releases/download/v0.0.1/kamatera-kamatera-0.0.0.tar.gz
```

Documentation for the modules is available via ansible-doc:

```
ansible-doc kamatera.kamatera.kamatera_compute
ansible-doc kamatera.kamatera.kamatera_compute_options
```

To use the collection, define the following environment variables:

```
export KAMATERA_API_CLIENT_ID=
export KAMATERA_API_SECRET=
```

Example playbooks:

* [Get available datacenters](https://github.com/OriHoch/ansible-collection-kamatera/blob/master/tests/compute_datacenters_playbook.yml#L1)
* [Get capabilities](https://github.com/OriHoch/ansible-collection-kamatera/blob/master/tests/compute_options_playbook.yml#L1)
* [Provision and manage servers](https://github.com/OriHoch/ansible-collection-kamatera/blob/master/tests/compute_playbook.yml#L1)

## Salt

[Salt](https://docs.saltstack.com/en/latest/) is a configuration managemenet and remote execution system.

The Kamatera module is pending approval by Salt, until it's approved it can be installed using Python:

```
pip install https://github.com/OriHoch/salt/archive/kamatera-cloud.zip
```

Documentation:

* [Using Salt Cloud](https://docs.saltstack.com/en/latest/topics/cloud/index.html)
* [Getting started with Kamatera for Salt Cloud](https://github.com/OriHoch/salt/blob/kamatera-cloud/doc/topics/cloud/kamatera.rst#getting-started-with-kamatera)
