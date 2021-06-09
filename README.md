[![CI](https://github.com/freuds/molecule-ansible-testing/workflows/CI/badge.svg?event=push)](https://github.com/freuds/molecule-ansible-testing/actions?query=workflow%3ACI)

# Molecule testing


you will need to additionally install Docker. Molecule requires an external Python dependency for the Docker driver which is provided when installing Molecule using pip install 'molecule[docker]'.


Create a new role with molecule:

	molecule init role myrole -d docker

	or with ansible-galaxy

	ansible-galaxy role init myrole

Ajouter à un role existant 

$ cd /path/to/roles/myrole
$ molecule init scenario --role-name myrole --verifier-name goss --driver-name vagrant --scenario-name vagrant

Then test it: 

	molecule test

And test it but leave the container running for debugging:

	molecule converge

Set a 'breakpoint' using `fail:` in the tasks.
