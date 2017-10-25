# udp-relay
One-way UDP relay with PID file

I needed a super-simple UDP relay to transmit AIS data from AIS receiver
running aisdispatcher (http://www.aishub.net/aisdispatcher-linux.php)
to AIShub network.

`udp-relay` The script itself. Place this to `/usr/local/bin/`

`centos/ais-relay` CentOS 5 init.d script. Place this to `/etc/init.d/`

`ubuntu/init.d/ais-relay` Ubuntu Xenial init.d script. Place this to `/etc/init.d/`. See Ubuntu install.
`ubuntu/default/ais-relay` Defaults for Ubuntu Xenial. Place this to `/etc/default/`

`udp-echo` Logger script based on `udp-relay`. Wrote this as `nc -u`
was blocking outputs for an unknown reason.

`centos/ais-logger` CentOS 5 init.d script for `udp-echo`

## Ubuntu install

After copying `ais-relay` files you need to say:

```
sudo update-rc.d ais-relay defaults 95
sudo systemctl daemon-reload
```

To start the service on boot say:

`sudo update-rc.d ais-relay defaults`
