# Ansible Playbook for Installing Netdata Agent

This playbook installs the Netdata Agent on specified hosts using the Kickstart method. 

## Variables
- `claim-token`: The claim token provided by Netdata.
- `claim-url`: The claim URL provided by Netdata.
- `channel`: The channel to use for the installation (stable, testing, or nightly).

## Tasks
1. Install `wget` as it is required for the Netdata Kickstart script.
2. Install the Netdata Agent via Kickstart script, using the provided claim token, claim URL, and channel.
3. Restart the Netdata Agent service on the server.

## Usage
1. Specify the hosts you want to install the Netdata Agent on in the `hosts` section.
2. Provide the `claim-token`, `claim-url`, and `channel` in the `vars` section.
3. Specify the remote user in the `remote_user` section.
4. Run the playbook using the command `ansible-playbook -i <inventory_file> <playbook.yml>`.
