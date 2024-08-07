# Cloud Practitioner Book

## 6 AWS Networking Services - VPCs, Route53, and CloudFront

* Key concepts:
    * CIDR: Classless Interdomain Routing

* Example:
    * VPC: 10.0.0.0/16
    * Subnet-1: 10.0.1.0/24
    * Subnet-2: 10.0.2.0/24

* Complex example (and most real):
    * VPC: 10.0.0.0/16 with its Internet Gateway
    * Availability Zone 1A:
        * Public Subnet 1: 10.0.1.0/24
        * Private Subnet 1: 10.0.2.0/24
    * Availability Zone 1B
        * Public Subnet 2: 10.0.3.0/24
        * Private Subnet 2: 10.0.4.0/24

* EC2:
    * In public subnet it will require a public IP address with a Load Balancer in front of it.
    * If you need a static IP address you need to configure your EC2 instance with a elastic IP address

* Security:
    * Security group:
        * Inbound and outbound rules
        * You can add up to five security groups
        * They are at instance level
        * They can accept itself traffic
        * They are stateless: you need to configure inbound and outbound rules
        * You can allow rules, but can not deny rules
        * You can separate the rules by protocols (HTTP, HTTPS, SSH)
    * NACL (Network Access Control Lists):
        * By default is configured in every VPC
        * By default it allows all inbound and outbound traffice
        * They are stateless: you need to configure inbound and outbound rules
    * NAT (Network Address Translation)
        * It works as a proxy
        * NAT Gateway allows to connect EC2 instances with private IPV4
    * VPC peering
        * Connection between two vpcs
        * They do not use the internet, for that reason they have greatest levels of bandwith
        * You can configure cross account and cross account regions
    * VPC transit gateway:
        * You can connect your VPC with a single point in VPC Transit Gateway
        * It follow a hub-and-spoke model
    * VPN Virtual Private Network:
        * You need to connect a Virtual Private Gateway
        * It depends of the internet and its velocity, AWS has a limit of 1.26 Gbps
    * Direct Connect:
        * Is a connecti with fiber optic.
        * You can get 1Gbps, 10Gbps or 100Gbps