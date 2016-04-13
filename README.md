# zaygrant

## What?

Minimal Vagrant environment for testing the current production/supported releases of:

 - CentOS
 - Ubuntu
 - Debian

Includes EPEL on CentOS and Universe/Multiverse on Ubuntu.

Also configures the VMs to have unique IPs behind the NAT so that they can reach each other.

Nothing special or unique here, but it lets you get up and running quickly without reading the whole [Vagrant tutorial](https://www.vagrantup.com/docs/getting-started/).

## How?

1. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
1. Install [Vagrant](https://www.vagrantup.com/downloads.html)
1. Install `git` if it's not already installed.
    * Mac: `brew install git`
    * Ubuntu: `apt-get install git`
    * RHEL/CentOS/\*EL: `yum install git`
1. Clone this repository somewhere.
1. `vagrant status`
1. `vagrant up <vm-name>` where `<vm-name>` is replaced with the name of the VM you wish to boot, from the list generated in the previous step.
1. Modify to your needs.

The above steps should be enough to get started for anybody running Mac OS X or Linux on their workstation.

For Windows, there are many useful tutorials on [the internet](https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=vagrant%20windows%20host). Google link provided not to be obnoxious, but to avoid giving a link to soon-to-be-dated instructions.

## Why?

I teach Puppet training classes, and often use Vagrant to test/demo things in those classes. Students often ask what Vagrant is, how they can use it, etc. This repository is intended for them to be able to get up and running with an SSH-reachable Linux VM very quickly, without having to learn much.

<a href="http://www.wtfpl.net/"><img src="http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-4.png" width="80" height="15" alt="WTFPL" /></a>
