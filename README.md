# Explore Packer

Little repo showing how to build a minimal Packer CentOS 7 image.

# Usage

```bash
packer build build.json
```

# Explanation

[Packer](https://www.packer.io/) is a tool to create VM images for multiple platform from a single configuration.  Given a description of the VM to create, e.g. ISO, kickstart files, Ansible, `packer` will build the VMs for multiple platforms and create VM images for VirtualBox, AWS, VMWare, Parallels, etc.

The `http/kickstart.cfg` file tells CentOS how to install, and `install.yml` is the [Ansible](https://www.ansible.com/) playbook for the post-install configuration.

This results in a [VirtualBox](https://www.virtualbox.org/) image of CentOS 7, with Grafana installed, ready to be started up in VirtualBox.
