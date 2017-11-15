# nvidia-fancontrol

Basic script that automatically controls NVIDIA GPU fans on a headless system for GNU/Linux.

# How does this work?

The script will try to detect all NVIDIA GPUs in the system and launch an X server on each of
them emulating an attached screen with the included EDID dump. It will then check in 10s
intervals wether the target temperature has been surpassed or not been reached yet. In either
case the script will adjust the fanspeed in steps up or down trying to maintain the target
temperature defined in defaults.

# Installation

```
install -D -m755 nvidia-fancontrol /opt/nvidia-fancontrol/nvidia-fancontrol
install -D -m755 nvidia-fancontrol-x /opt/nvidia-fancontrol/nvidia-fancontrol-x
install -D -m644 nvidia-fancontrol.default /etc/default/nvidia-fancontrol
install -m644 dfp-edid.bin /opt/nvidia-fancontrol/dfp-edid.bin
install -m644 xorg.conf /opt/nvidia-fancontrol/xorg.conf
```

Edit /etc/default/nvidia-fancontrol to your liking.

# How to run

Simply run the following as a user privileged enough to run an X server:

```
/opt/nvidia-fancontrol/nvidia-fancontrol
```

Check /var/log/nvidia-fancontrol.log for how the script does.

# TODO

* service via systemd (start/stop etc)
* log levels

# Donations:

```
BTC: 34qmK6ZKX5WeT7winCayv2HVVxZnnwnsot
XMR: 4361xpTjBvBCArk43wKiSFiR4vu2aTXu3EgKF7iATHZfYZatDyhoQ6h3JMV4WZkxusL22Ri3ZXY8MWdN48T4z8prFnWt7PF
```
