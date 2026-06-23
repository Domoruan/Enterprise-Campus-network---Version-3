# Campus-network
Enterprise Campus Network I designed and configued from scratch.

# Cisco Packet Tracer enterprise network connecting an HQ building and a Branch building using OSPF.

## Main Features

- VLAN segmentation and inter-VLAN routing
- OSPF Area 0 routing between HQ and Branch
- TACACS+ centralized device authentication
- Cisco ASA firewall
- NAT/PAT for HQ and Branch Internet access
- Cisco CME VoIP
- Wireless LAN Controller
- DHCP, DNS, email, web, and AAA services
- HSRP provides redundancy between the primary and backup HQ Layer 3 switches.
- The switches share virtual gateway addresses for the HQ VLANs.

### TACACS+ Login
  
TACACS+ is used for HQ L3 switch and backup L3 switch login. 'Enable' authentication remains local.

## Email Services

The server VLAN includes a simulated email service for testing communication between users in the Packet Tracer environment. Confirmed operational.

## VoIP Service

The network includes a dedicated voice VLAN and Cisco Call Manager Express for IP phone communication.

- Extension 1001 is successfully registered and operational.
- Extension 1002 receives an IP address but is still being troubleshot for CME registration.

## Firewall

A Cisco ASA firewall protects the campus network and connects it to the ISP.

- Unsolicited inbound traffic is blocked
- Stateful ICMP inspection is enabled

## NAT/PAT

Dynamic PAT provides Internet access for both HQ and Branch networks.

- HQ devices can reach the ISP
- Branch devices can reach the ISP
- Internal addresses are translated through the ASA outside interface

## Routing

- Routing protocol: OSPF Area 0
- HQ-to-Branch routed link: `10.0.0.0/30`
- BGP was removed because both buildings are part of the same campus network

## Wireless
The HQ site includes a Wireless LAN Controller for centralized wireless management.

- The WLC management address is 192.168.30.10.
- Wireless service is currently configured at HQ.
- Branch wireless deployment was tested but is not yet part of the final design. Branch endpoints are connecting to HQ AP.
  
## Planned Improvements
This project is still a work in progress. Future updates will include:

- Expanding TACACS+ authentication to all routers and switches
- Resolving the remaining VoIP registration issue for extension 1002
- Continuing to improve the overall network design and documentation
