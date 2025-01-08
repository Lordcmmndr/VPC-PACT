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

#### About the Author
This project was created by **Michael Emeruwa**, a student at NextWork.org, as part of a hands-on learning experience.

"Everyone should be in a job they love." Check out [NextWork.org](https://nextwork.org) for more projects and resources.
