# dotfiles
collection of different config files

## grub config
### Suspend-to-RAM
Seems like `/etc/default/grub` is not present anymore. The configs have moved to `/etc/default/grub.d/02-tuxedo.cfg`.
So, in order to change the sleep mode to Suspend-To-RAM,  add the `mem_sleep_default=deep` to that.
```
sed -ie 's/GRUB_CMDLINE_LINUX_DEFAULT="\(.*\)"/GRUB_CMDLINE_LINUX_DEFAULT="\1 mem_sleep_default=deep"/' /etc/default/grub.d/02-tuxedo.cfg 
update-grub
```
