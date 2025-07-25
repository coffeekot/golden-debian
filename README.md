# golden-debian

This is a collection of automations I use for a small-scale Debian server.

## Includes (so far):

### Automated OS installation (Debian 12)

- Use preseed.cfg to bake configuration into ISO.
- Preseed needs some replacements (marked {{REPLACE_ME}}):
	- User password: `mkpasswd -m sha-512`
	- SSH authorized key
- Configured specifically for virt-manager (uses /dev/vda for installation)
- More information:
	- [Preseed file configuration](https://www.debian.org/releases/stable/amd64/apbs04.en.html)
	- [Baking preseed into ISO](https://wiki.debian.org/DebianInstaller/Preseed/EditIso)

### Ansible playbooks

- Playbooks use relative local paths.
- Playbooks install nginx and deploy a simple http site.
- Need to either re-configure Ansible or use default folders I set up for:
	- Private key
	- Hosts file
	- Useful to filter out the noise in cfg file: `grep -v -e "#" -e ";" ansible/ansible.cfg | awk NF`
