# iptables boot

`iptables-boot` is an `init.d` service that automatically saves `iptable` rules when the system shutdowns and restores them to the saved value after powering up.


## Installation

From a command prompt, run as root (e.g. using `sudo`):
~~~bash
#  cp iptables-boot /etc/init.d/
#  update-rc.d iptables-boot defaults
#  service iptables-boot start
~~~


## Usage

The rules are persisted in `/etc/iptables.boot`. If no persisted rules file exists, `iptables-boot` adopts the current `iptables` rules.

To force saving the rules at any time, run as root:
~~~bash
#  service iptables-boot restart
~~~
