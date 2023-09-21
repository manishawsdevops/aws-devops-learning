# VPC Implementation, CIDR Range, and Troubleshooting



## Part 1 : VPC Setup

### Steps

1. Creating a VPC called my-vpc-01

![VPC](vpc.png)

2. Creating Public and Private Subnets

![Public Subnets and Private Subnet](Subnets.png)

3. Creating an Internet Gateway and attaching to vpc-01

![Internet Gateway](IGW.png)

4. Creating Route Tables for public subnets and private subnet

![Public Route Table and Private Route Table](RTs.png)
 
5. Configure Public Route Table to route traffic to Internet Gateway

![Public Route Table Routing](pubrtIGW.png)

6. Attaching Public Route Table to Public Subnets

![Public Route Table to Public Subnets](pubrtSubnets.png)

7. Creating Security Groups for public and private instances
   and defined inbound rules for each.
![Security Groups](SG.png)
![Public Security Group](pubSG.png)
![Private Security Group](privateSG.png)

## Part 2 : Instance Launch and Troubleshooting

8. Launching 2 Public Instances in 2 Public Subnets and Private Instance in Private Subnet

![Public Instances and Private Instance](Instances.png)

9. Checking each Public Instance is connecting through internet

![Public Instance1 to Internet Gateway](pub1IGWtest.png)
![Public Instance2 to Internet Gateway](pub2IGWtest.png)

10. Checking Private Instance is connecting through internet

![Private Instance to Internet Gateway](privateIGWtest.png)

11. Creating NAT Gateway and connecting to private route table

![NAT Gateway](natgw.png)
![Subnet Association](privateRTsubnet.png)

12. Private Instance is connected to Internet via NAT Gateway

![Private Instance to Internet](privateIGW.png)

# Part 3 : CIDR Range Calculation

Question : Given a requirement to accommodate 150 host addresses in a subnet, calculate the appropriate CIDR      block (prefix length) to fulfill this requirement.Provide the CIDR notation and subnet mask for the selected CIDR block.

Answer : There are 32 bits in total network
         24 bits out of 32 are locked i.e., 32-24=8 bits is used as host bits.
         2^8=256 addresses are present
         Out of 256 , 2 addresses are used as network address which is least and broadcast address which is the highest.
         For example :
         Chosen address : 10.0.0.0/24
         10.0.0 ==> These are locked, we can't change these 24 bits
         .0 ==> this last 8 bits we can use as host addresses
         (2^8)-2 = 256-2 = 254 usable host addresses
         In this 254 host addresses, 150 host addresses can be accomodated.

         CIDR notation : 10.0.0.0/24
         Subnet mask : 11111111.11111111.11111111.00000000
         Network Address : 10.0.0.0
         BroadCast Address : 10.0.0.255
         Usable Host Addresses : 10.0.0.1 to 10.0.0.254

# Part 4 : Diagram
         
# Virtual Private Cloud Flow Diagram

![VPC Network](VPC%20diagram.png)