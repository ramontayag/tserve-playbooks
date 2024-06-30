Start by installing openssh in the server and connecting to it.

```
ssh username@ip.com
```
 
The rest can be done remotely. In the server:
 
```
sudo apt-get clean && \
sudo apt-get upgrade && \
sudo apt-get update -yqq && \
  sudo apt-get install ansible-core
```

Then download the Ansible playbooks:

```
git clone https://github.com/ramontayag/tserve-playbooks.git
cd tserve-playbooks
```

Now it's time to setup the basics:

```
sudo ansible-playbook --connection=local setup.yml
```

Install docker:

```
sudo ansible-playbook --connection=local docker.yml
```
