### Ansible role - openvpn-client  ----- hasn't finished  
- Ansible role which install and configure OpenVpn on Ubuntu 
- Install and setup openvpn 
- Create clients configuration file
### Variables
<pre>
   #settings
 openvpn_etcdir: /etc/openvpn             # openvpn dir
 openvpn_server_addr: 192.168.252.128     # The server address
 openvpn_port: 1194                       # The server port
 openvpn_protocol: udp                    # Protocol , use udp or tcp
 openvpn_device: tun                      # Virtual network driver TUN or TAP
 openvpn_log: /var/log/openvpn.log        # Log's directory
 openvpn_comp_lzo: yes                    # Enable compression yes or no
 openvpn_status: openvpn-status.log       # status log of openvpn service
 openvpn_verb: 3                          # verbose mode
 openvpn_reneg_sec: 259200
 openvpn_user: nobody
 openvpn_group: nogroup
 openvpn_use_pass: 123456                 # private password
 # <- paste certificates content or path(if your send certs to client) : for example ~/etc/openvpn/ca.crt
 ca_cert:                                 # <-
 client_cert:                             # <-
 client_key:                              # <-
 tls_auth_key:                            # <-
 # <-
</pre>

### Usage 
<pre>
- hosts: all
  roles:
  - openvpn-client
    vars: 
    </pre>
