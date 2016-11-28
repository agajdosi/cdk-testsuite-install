# cdk-testsuite-install

### Preparation:

* Create RHEL group in /etc/ansible/hosts:
```
[rhel]
url.to.machine
```
* In install_virtualization.yaml file edit username and password under which the machine will be registred
* Replace file auth-key with your public key

### Usage:
1. cd into cdk-testsuite-install
2. run "ansible-playbook create_user.yaml" to create testing user named "cdk"
3. run "ansible-playbook install_virtualization.yaml" to register system and install 3rd party components for CDK
4. run "ansible-playbook install_CDK.yaml" to install latest nightly CDK and add rhel box into vagrant
5. run "ansible-playbook install_avocado.yaml" to install avocado and setup adb-tests/cdk-testsuite


### To do:
1. Make it more "nice and clean"
2. Support workstation and server variant
