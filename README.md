TOOLS
-------

Tools and Scripts I have written to make my life easier. YMMV with anything that is included here.

## vminstall

To use this script, you will need KVM (libvirt) installed with the `virt-install` commands available. To use the script, place it somewhere in your `$PATH` (such as `$HOME/.local/bin/` or `/usr/local/bin/`).

This script assumes you have a kickstart available at `$HOME/Repositories/kickstarts/`. Currently the two kickstart files are assumed to be `ks-el7.cfg` or `ks-el8.cfg`.
This script also assumes that DVD ISO files are available in `/var/lib/ibvirt/images/` in a directory structure as follows:

```
centos
├── 7
│   ├── centos7.iso -> /var/lib/libvirt/images/rhel/7/centos-everything-dvd.iso
│   └── centos-everything-dvd.iso
└── stream8
    ├── centos-stream8-dvd.iso
    └── cs8.iso -> /var/lib/libvirt/images/centos/stream8/centos-stream8-dvd.iso
rhel
├── 7
│   ├── rhel7.iso -> /var/lib/libvirt/images/rhel/7/rhel-server-7.9-x86_64-dvd.iso
│   └── rhel-server-7.9-x86_64-dvd.iso
└── 8
    ├── rhel-8.3-x86_64-dvd.iso
    └── rhel8.iso -> /var/lib/libvirt/images/rhel/8/rhel-8.3-x86_64-dvd.iso
```

As new versions of the OS come out, update the DVD install ISO files that the symlink points to.

NOTE: The script is still a WIP. Things probably will change and potentially break.
