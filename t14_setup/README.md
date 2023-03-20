# This playbook will setup the T14 as a daily driver using Fedora. In general it will:

1. Install a bunch of rpms to include cockpit, start their services, and allow them the the FW.

1. Install some bluetooth drivers and configure bluetooth so that airpod pros work.

1. Configure flatpak and install zoom & podaman desktop.

1. Create some housekeeping dirs.

## VPN

- I did not feel comfortable putting the vpn rpms on git so just authenticate and follow the instructionser [here](https://redhat.service-now.com/help?id=kb_article_view&sysparm_article=KB0005424)
