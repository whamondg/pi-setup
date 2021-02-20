# Raspberry-setup

Setup a new Raspberry PI using Ansible.

## Prerequisites

 - Boot the Raspberry PI to the setup screen
 - Configure WiFi
 - Install Raspbian
 - Note the IP address of the PI (should be on the start screen)
 - Complete the Raspbian setup process and change the default password (raspberry) to something else
 - Go to the preferences and enable SSH

## Setup SSH keys

On a remote computer check for existing keys in ~/.ssh and if none are present then [https://www.ssh.com/ssh/keygen](generate a new key pair).

Copy the public key to the PI: `ssh-copy-id user@ip`.

## Setup Hosts

  Rename hosts.template to hosts and add individual host entries for each PI.

  Test the host connections by running `ansible-playbook -i hosts testConnection.yml`

## Configure the PIs

  Run `ansible-playbook -i hosts bootstrap.yml`




