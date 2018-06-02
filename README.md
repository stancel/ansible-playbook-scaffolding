ansible-playbook-scaffolding
=========

This repos holds a skeleton/scaffolding structure for creating Ansible playbooks based on the [recommended directory layout] (http://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html#directory-layout). To use this just clone this repo and name it to whatever you want, remove the .git folder, 


How to Use
------------

To use this playbook just run this command.

	1. `ansible-galaxy install -r requirements.yml` - Assumes you have external roles install
	2. `ansible-playbook master.yml --inventory-file=/path/to/inventory`


Requirements
------------

Place any requirements here, if any, for running this playbook.

Variables
------------

Give information about what variables must be filled out to run this playbook along with where to fill them out.


Roles
------------

If you plan to create any roles for this playbook and not just pull in ones you have already written or public ones from Ansible Galaxy, then I would highly recommend using the Ansible Galaxy CLI to create the proper scaffolding/skeleton structure for each of your roles.

	`ansible-galaxy init name-of-your-role`

