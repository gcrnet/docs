# The gcrNet Network

## The Logical Network

The gcrNet is a dedicated research network that can be accessed from both UNC Greensboro and NC A&T State University. The network core is connected to the internet via a 10G link with distribution at each campus. Scientific insturmentation is connected to gcrNet nodes (switches) located at UNC Greensboro, NC A&T State University, and the Joint School of Nanoscience and Nanoengineering.

The internal network is connected at 100G and supports high speed transfers from insturmentation to the Data Transfer Node. Globus is then available to facilitate high speed transfer to and from the gcrNet.

## The Physical Network

The physical network is deployed across the UNC Greensboro main campus, the Joint School of Nanoscience and Nanoengineering (JSNN), and the North Carolina State A&T University main campus. Information on physical locations where the gcrNet is available can be found below:

| Campus | Building | Floor | Notes |
| ----- | -------- | ----- | ----- |
| UNC Greensboro | McNutt | 1st | Core network, inside the datacenter |
| JSNN | ?? | 1st | 102 Lab |
| UNC Greensboro | Pettey | TBD | |
| UNC Greensboro | Sullivan Science | TBD | |

## External Access

The gcrNet network can be accessed from both the UNC Greensboro and NC A&T State University networks. The gcrNet allows SSH access from both networks to genlogin.gcrnet.org. A VPN is planned but not yet available for remote access. 

Inbound and outbound access to the gcrNet is limited by router ACLs and not a stateful firewall. This allows the gcrNet to operate at high speed and support the transfer of large data sets to peer Sceince DMZ networks. Router ACLs provide less flexibility than a stateful firewall general internet access cannot be supported and therefore applications that require general internet access are not suitable for the gcrNet.

Additional information on accessing the gcrNet can be found by visting the Getting Started page.

## Common Hostnames

| Server | IPv4 | IPv6 | Accessible From | Description |
| ------ | ---- | ---- | --------------- | ----------- |
| *hostname* | 127.0.0.1 | | Internal | What does it do? |
| ns1.gcrnet.org | 152.13.0.13 | 2600:2701:1010:500::100 | External | IPAM, DNS, NAT64 server for gcrNet
| genlogin.gcrnet.org | 152.13.0.11 | 2600:2701:1010:500::110 | External | General Login Node
| dtn01.gcrnet.org | 152.13.0.12 | 2600:2701:1010:500::111 | External | Data Transfer Node - Globus
| uncg-mcnuttperf01.gcrnet.org | 152.13.0.14 | 2600:2701:1010:500::112 | External | PerfSonar Node (McNutt)
| uncg-jsnnperf01.gcrnet.org | 152.13.0.15 | 2600:2701:1010:500::113 | External | PerfSonar Node (JSNN)
| gcrnetapp01.gcrnet.org | 152.13.0.16 | 2600:2701:1010:500::114 | External | LDAP/COmanage
