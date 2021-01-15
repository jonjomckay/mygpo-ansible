mygpo-ansible
=============

A set of Ansible configurations to set up and run a production-level installation of [gpodder's mygpo](https://github.com/gpodder/mygpo).

## Running

```
# Clone the repository
git clone git@github.com:jonjomckay/mygpo-ansible.git

# Set up a virtualenv
python3 -m venv venv

# Activate the virtualenv
source venv/bin/activate

# Install Ansible stuff
pip install -r requirements.txt
ansible-galaxy install -r requirements.yml

# Configure the inventory to point to your node(s)
nano inventory

# Install a development instance
ansible-playbook -i inventory --extra-vars env=dev playbook-mygpo.yml
```