# k8s-services-deploy-ansible
Holds my the ansible playbook for automatically deploying any microservice architecture configuration on k8s

A .kubeconfig file needs to be present in the folder in order to connect to the k8s cluster

The ansible playbook automatically creates the namespace and deploys, according to definitions:
 - services
 - service accounts
 - deployments

REQUIREMENTS:
 - python3
 - virtenv

INSTALLATION:
 - Create a python virtenv: python3 -m venv ansible
 - Enter the virtenv: source ansible/bin/activate
 - RUN: python3 -m pip install ansible openshift

USAGE:
 - In deployment.yml change value of the namespace_def variable with your namespace name.
 - Create a service.definitions.yml file with the definitions of the different services that you need. Use service.definitions.template.yml as reference
 - RUN: source ansible/bin/activate
 - RUN: ansible-galaxy collection install -r requirements.yml
 - RUN: ansible-playbook playbook.yml

