
# AWS VPC Networking Project

This repository showcases the steps I took to configure a Virtual Private Cloud (VPC) in AWS, along with setting up a subnet, Internet Gateway, Route Table, Security Groups, and Network ACLs (NACLs). This project allowed me to deepen my understanding of AWS networking and cloud security practices.

## Project Overview

In this project, I successfully configured the following components:

- **VPC**: Created a custom Virtual Private Cloud with a CIDR block of `10.0.0.0/16`.
- **Subnet**: Deployed a public subnet with a CIDR block of `10.0.1.0/24` within the VPC.
- **Internet Gateway**: Attached an Internet Gateway to the VPC to enable internet access.
- **Route Table**: Configured routing by creating a custom route table and associating it with the subnet.
- **Security Groups**: Set up stateful security groups to manage traffic at the resource level.
- **Network ACLs**: Created and configured NACLs to provide an additional layer of security at the subnet level.

## Steps Taken

1. **VPC Creation**: 
   - I started by creating a VPC to define my own isolated network in AWS. The CIDR block I chose (`10.0.0.0/16`) provided me with a large IP address range.

2. **Subnet Setup**:
   - I created a public subnet within the VPC with a CIDR block of `10.0.1.0/24`, which provided me with 256 IP addresses for instances within the subnet.

3. **Internet Gateway Attachment**:
   - I created an Internet Gateway and attached it to my VPC. This was necessary to enable instances in the public subnet to communicate with the internet.

4. **Route Table Configuration**:
   - After creating a custom route table, I added a route that directed all outbound internet traffic (`0.0.0.0/0`) through the Internet Gateway. I then associated this route table with my public subnet.

5. **Security Groups**:
   - I configured security groups to allow specific types of traffic (like HTTP and SSH) to reach my instances. By default, outbound traffic is allowed, so I only focused on configuring inbound rules.

6. **Network ACLs**:
   - I created custom Network ACLs to add a stateless layer of security at the subnet level. I added rules for both inbound and outbound traffic for the public subnet.

## Reflection

This project helped me solidify my understanding of AWS networking components, particularly the differences between stateful security groups and stateless NACLs. I now have hands-on experience with creating a secure VPC environment, setting up public subnets, and configuring routing and security for cloud-based resources.

## Next Steps

I plan to further enhance this project by deploying EC2 instances within the subnet, configuring auto-scaling groups, and experimenting with private subnets and NAT Gateways to manage instances that don't need direct internet access.

## Project Screenshots

![3](https://github.com/user-attachments/assets/0985e285-5545-41b9-8f74-962277adfcdd)

