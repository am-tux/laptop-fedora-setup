# This playbook will setup a laptop as a daily driver using Fedora. 
  ## In general it will:

1. Install a bunch of rpms (cockpit, vscode, packer, chrome, etc). Start their services, and allow them through the FW.

1. Install some bluetooth drivers and configure bluetooth so that airpod pros work.

1. Configure flatpak, install zoom & podman desktop.

1. Set up git user name and email so that it does not complain later.

1. Create some housekeeping dirs.

## VPN

- Did not feel comfortable putting the vpn rpms on git. So just authenticate and follow the instructions [here](https://redhat.service-now.com/help?id=kb_article_view&sysparm_article=KB0005424)

## Assumptions/Requirements

- Per the work guidelines, be sure to encrypt the filesystem (this can only be done at install).
- **Change the default vars in the git config role unless you want to be Andrew.**
  - Same with the housekeeping dirs role
- Assuming that you'll run this role:
  - As the user that you will use the laptop as.
    - Who has sudo access.
  - From another machine.
- Easiest way to stage this:
  1. Create the user via the fedora installation guide.
  1. Log in physically once, and allow ssh access via etc/ssh/sshd_config `PasswordAuthentication yes).`
  1. Can turn (PasswordAuthentication) off again after running the play.

## Random links/Notes/TODO

- [Night Theme Switcher](https://extensions.gnome.org/extension/2236/night-theme-switcher/)
- Might add disa-stig later...
- Want to automate little tweaks like (ctrl + e) opening the file browser.
- Joining the system to quay and all that goodness.
- Last used against Fedora 38.
