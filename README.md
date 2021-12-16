**Pynventory**

Create a DokuWiki Linux Server inventory table:

```
# pynventory --help
usage: pynventory 192.168.1.0/24 --hostname --cpu_cores --memory

Create a DokuWiki friendly inventory table or system hostfile of your servers

positional arguments:
  ip_range              CIDR IP range. ie: 192.168.0.0/24

optional arguments:
  -h, --help            show this help message and exit
  --format {dokuwiki,hostfile}
                        Choose the output format. Option "hostfile" ignores all additional checks but forces --hostname
  --cpu_cores
  --hostname
  --os_version
  --ntp_host
  --memory
  --disk
  --kernel
  --link_host LINK_HOST
                        create link to a new page for host description with this as base url
  --link_empty_host     create links for nonexistent hosts
  --user SSH_USER       ssh user
  --report_errors       Report connection failures (except for timeout) to stdout
  -d                    enable verbose output to stderr
```

or output the hostnames in a hostfile compatible format with:
```
# pynventory  192.168.247.0/24 --user root --format hostfile
```
