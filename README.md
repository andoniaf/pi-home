# pi-home

## First step
Add ssh keys to avoid use user/password to connect:
```
mkdir ~/.ssh && curl -s https://github.com/andoniaf.keys > ~/.ssh/authorized_keys
```


---
## Services
### OpenVPN
Based on [kylemanna/docker-openvpn](https://github.com/kylemanna/docker-openvpn)

### Pi-hole
Based on [pi-hole/docker-pi-hole](https://github.com/pi-hole/docker-pi-hole)

- Local DNS config:

    `etc-dnsmasq.d/02-lan.conf`
    ```
    addn-hosts=/etc/pihole/lan.list
    ```

    `etc-pihole/lan.list`
    ```
    192.168.1.3 antman
    192.168.1.4 wasp
    ```

