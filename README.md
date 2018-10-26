ansible-playbook-scaffolding
=========

This repos holds a skeleton/scaffolding structure for creating Ansible playbooks based on the [recommended directory layout](http://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html#directory-layout). To use this just clone this repo and name it to whatever you want, remove the .git folder, and start creating your playbook.


How to Use
------------

To use this playbook just run this command.

	1. ansible-galaxy install -r requirements.yml -p roles/ --force
	2. Create a file called .vault_pass in this folder and put a random string in it for decrypting your sensitive variables. Something like: QSkngTv#KTJ=WXpg6qVR
	3. Fill out needed variables in vars/all_vars.yml and vars/vault.yml files
	4. ansible-vault encrypt vars/vault.yml   #Encrypt the sensitive variables
	5. ansible-playbook master.yml -e @vars/all_vars.yml -e @vars/vault.yml -i hosts/production


Requirements
------------

Place any requirements here, if any, for running this playbook.

Variables
------------

See the `vars/all_vars.yml` and `var/vault.yml` files for all of the needed variable values to fill out.


Roles
------------

If you plan to create any roles for this playbook and not just pull in ones you have already written or public ones from Ansible Galaxy, then I would highly recommend using the Ansible Galaxy CLI to create the proper scaffolding/skeleton structure for each of your roles.

	ansible-galaxy init name-of-your-role

