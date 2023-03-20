# This playbook will setup a laptop as a daily driver using Fedora. In general it will:

1. Install a bunch of rpms to include cockpit, start their services, and allow them through the FW.

1. Install some bluetooth drivers and configure bluetooth so that airpod pros work.

1. Configure flatpak, install zoom & podaman desktop.

1. Set up git user name and email so that it does not complain later.

1. Create some housekeeping dirs.

## VPN

- Did not feel comfortable putting the vpn rpms on git. So just authenticate and follow the instructionser [here](https://redhat.service-now.com/help?id=kb_article_view&sysparm_article=KB0005424)

## Assumptions/Requirements

- Assuming that you'll run this role as the user that you will use the laptop as, who has sudo access.
- Easiest way to stage this is to create the user via the fedora installation guide. Log in once, and allow ssh access via /etc/ssh/sshd_config (PasswordAuthentication yes).
  - Can turn (PasswordAuthentication) off again after running the play.

## Random links/Notes

- [Night Theme Switcher](https://extensions.gnome.org/extension/2236/night-theme-switcher/)
- Might add disa-stig later...
- Might configure the auto-updating in the future
- Last used against Fedora 37
