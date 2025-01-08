# VPC-PACT
Exploring private networks
# Build a Virtual Private Cloud (VPC)

This repository contains instructions and insights for building a Virtual Private Cloud (VPC) on Amazon Web Services (AWS), an essential component for networking and resource control in the cloud.

## What is Amazon VPC?
Amazon VPC (Virtual Private Cloud) allows you to create a private network within AWS. This network provides control over who can access and interact with resources inside the VPC, enabling secure management of cloud-based resources.

## Project Overview
This project demonstrates:
1. Setting up an Amazon VPC with a custom CIDR block.
2. Creating subnets (both public and private) within the VPC.
3. Attaching an Internet Gateway to enable public internet access.

### Steps to Build a VPC

#### 1. Create a VPC
- Navigate to the AWS VPC Console.
- Define an IPv4 CIDR block, a unique IP address range for the VPC to identify and exchange data with resources.
- Note: AWS provides a default VPC upon account creation, but this guide focuses on creating a custom VPC.

#### 2. Configure Subnets
- Subnets are subdivisions within a VPC to group resources with similar access rules.
- Public Subnet:
  - Enable auto-assign public IPv4 addresses to allow public internet access.
  - Attach to an Internet Gateway for external accessibility.
- Private Subnet:
  - Not accessible to the public. Reserved for internal resources only.

#### 3. Attach an Internet Gateway
- An Internet Gateway serves as a bridge between the VPC and the internet.
- To enable internet access:
  - Create an Internet Gateway in the AWS VPC Console.
  - Attach it to your custom VPC.

### Time Taken
- Building the VPC and configuring its components: ~30 minutes.

### Common Terms
- **CIDR Block**: Defines the IP address range for your VPC.
- **Public Subnet**: Accessible to the public via the internet.
- **Private Subnet**: Isolated and only accessible within the VPC.
- **Internet Gateway**: Enables external users to access resources in the VPC.

### Additional Resources
- [AWS VPC Documentation](https://aws.amazon.com/vpc/documentation/)
- [My NextWork Portfolio](https://community.nextwork.org/c/i-have-a-question?automatic_login=true)

---
# VPC Traffic Flow and Security

This repository contains details and instructions for configuring traffic flow and security within an Amazon Virtual Private Cloud (VPC) on AWS.

## What is Amazon VPC?
Amazon VPC (Virtual Private Cloud) is a private network in the cloud. It enables users to control how traffic interacts with resources within the network, ensuring secure and efficient data exchange.

## Project Overview
This project focuses on:
1. Configuring route tables for data pathways.
2. Setting up security groups to regulate traffic at the resource level.
3. Applying network ACLs to manage traffic rules for entire subnets.
4. Understanding default and custom configurations for traffic control.

### Steps to Configure VPC Traffic Flow and Security

#### 1. Set Up Route Tables
- Route tables define pathways for data to move within the VPC and externally.
- Example: To route internet-bound traffic, define a route with:
  - **Destination**: `0.0.0.0/0`
  - **Target**: Attached Internet Gateway (e.g., `igw-012a0ad20563af3f`)

#### 2. Configure Security Groups
- Security groups act as firewalls for individual resources in the VPC.
- Rules:
  - **Inbound Rules**: Control incoming traffic. Example: Allow HTTP traffic (Type: HTTP, Source: Anywhere-IPv4).
  - **Outbound Rules**: Control outgoing traffic. By default, all outgoing traffic is allowed.

#### 3. Set Up Network ACLs (Access Control Lists)
- Network ACLs provide broader traffic control at the subnet level.
- Default ACL:
  - Inbound and outbound rules allow all traffic.
- Custom ACL:
  - Inbound and outbound rules deny all traffic unless explicitly customized.

#### 4. Security Groups vs. Network ACLs
- **Security Groups**: Granular control over individual resource traffic.
- **Network ACLs**: Broad traffic rules applied at the subnet level.

### Common Challenges
- **Default Deny Rules**: By default, custom security groups and network ACLs deny all traffic. Ensure to configure necessary rules for intended access.

### Time Taken
- Configuring VPC traffic flow and security: ~40 minutes.

### Additional Resources
- [AWS VPC Documentation](https://aws.amazon.com/vpc/documentation/)
- [My NextWork Portfolio](https://community.nextwork.org/c/i-have-a-question?automatic_login=true)

---

#### About the Author
This project was created by **Michael Emeruwa**, a student at NextWork.org, as part of a hands-on learning experience.

"Everyone should be in a job they love." Check out [NextWork.org](https://nextwork.org) for more projects and resources.

#### About the Author
This project was created by **Michael Emeruwa**, a student at NextWork.org, as part of a hands-on learning experience.

"Everyone should be in a job they love." Check out [NextWork.org](https://nextwork.org) for more projects and resources.
