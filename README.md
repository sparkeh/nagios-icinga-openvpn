# nagios-icinga-openvpn

Nagios/Icinga check for OpenVPN availability monitoring

## What to do with the check
The checks must be run on the monitoring server

## How to use check_openvpn
The plugin is a normal check which must be run on the monitoring server. It queries the target OpenVPN server and outputs OK, etc.
```
$ ./check_openvpn -h
usage: check_openvpn [-h] [-p PORT] [-t] [--timeout TIMEOUT] [--digest DIGEST]
                     [--digest-size DIGEST_SIZE]
                     [--digest-key-client DIGEST_KEY_CLIENT]
                     [--digest-key-server DIGEST_KEY_SERVER]
                     [--tls-auth TLS_AUTH] [--tls-auth-inverse] [--validate]
                     host

positional arguments:
  host                  the OpenVPN host name or IP

optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  set port number (default is 1194)
  -t, --tcp             use tcp instead of udp
  --timeout TIMEOUT     set timeout (default is 5)
  --digest DIGEST       set digest algorithm (default is "sha1")
  --digest-size DIGEST_SIZE
                        set HMAC digest size
  --digest-key-client DIGEST_KEY_CLIENT
                        set client HMAC key
  --digest-key-server DIGEST_KEY_SERVER
                        set server HMAC key for packet validation
  --tls-auth TLS_AUTH   set tls-auth file
  --tls-auth-inverse    set tls-auth file direction to inverse (1)
  --validate            validate response
```
