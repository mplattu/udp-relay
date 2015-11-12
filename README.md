# udp-relay
One-way UDP relay with PID file

I needed a super-simple UDP relay to transmit AIS data from AIS receiver
running aisdispatcher (http://www.aishub.net/aisdispatcher-linux.php)
to AIShub network.

`udp-relay` The script itself. Place this to `/usr/local/bin/`

`ais-relay` CentOS 5 init.d script. Place this to `/etc/init.d/`

`udp-echo` Logger script based on `udp-relay`. Wrote this as `nc -u`
was blocking outputs for an unknown reason.

`ais-logger` CentOS 5 init.d script for `udp-echo`
