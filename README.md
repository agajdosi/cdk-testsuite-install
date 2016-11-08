# cdk-testsuite-install

### Preparation:

* Create RHEL group in /etc/ansible/hosts:
```
[rhel]
url.to.machine
```
* In install_virtualization.yaml file edit username and password under which the machine will be registred
* Replace id_rsa.pub with your public key

### Usage:
1. cd into cdk-testsuite-install
2. run "ansible-playbook create_user.yaml" to create testing user named "cdk"
3. run "ansible-playbook install_virtualization.yaml" to register system and install 3rd party components
4. run "ansible-playbook install_CDK.yaml" to install latest nightlly CDK and add rhel box into vagrant


### To do:
1. Installation of Avocado and cdk-testsuite
2. Make it more "nice"
