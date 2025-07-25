# golden-debian

This is a collection of automations I use for a small-scale Debian server.

## Includes (so far):

### Automated OS installation (Debian 12)

- Use preseed.cfg to bake configuration into ISO.
- Preseed needs some replacements (marked {{REPLACE_ME}}):
	- User password: `mkpasswd -m sha-512`
	- SSH authorized key
- Configured specifically for virt-manager (uses /dev/vda for installation)

## More information:

- [Preseed file configuration](https://www.debian.org/releases/stable/amd64/apbs04.en.html)
- [Baking preseed into ISO](https://wiki.debian.org/DebianInstaller/Preseed/EditIso)
