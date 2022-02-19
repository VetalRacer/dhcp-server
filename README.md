# Configure dhcpd-server and client

Steps for Virtual Box VMs:
- Create new network with CIDR: 192.168.30.0/24
- Off DHCP for this network
- Create 2 VM with Ubunti 20.04:
    1. dhcpd-server vm use Adapter1 as Bridge and Adapter2 as NAT network with new network
    2. dhcp-client vm use Adapter2 as Bridge
- Change ip for VMs and users in hosts file
- Run asndible-playbook playbooks/dhcpd-server.yml
- Change for dhcp-client vm Bridge adapter to Nat network