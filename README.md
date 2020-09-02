# Deploying-the-MySQL-and-Wordpress-architecture-on-AWS-instance

![alt text](https://2.bp.blogspot.com/-M5mou_8yyl4/XDLK-2xxWtI/AAAAAAAACeI/f4o3_L2PzP0Q8lVqzpAJ4W25GMdQzUOSwCLcBGAs/s1600/sample%2Bvpc.jpg)

**Project Description**
-Steps:
- Write a Infrastructure as code using terraform, which automatically create a VPC.

- In that VPC we have to create 2 subnets:
    a)  public  subnet [ Accessible for Public World! ] 
    b)  private subnet [ Restricted for Public World! ]

- Create a public facing internet gateway for connect our VPC/Network to the internet world and attach this gateway to our VPC.

- Create  a routing table for Internet gateway so that instance can connect to outside world, update and associate it with public subnet.

- Launch an ec2 instance which has Wordpress setup already having the security group allowing  port 80 so that our client can connect to our wordpress site.
Also attach the key to instance for further login into it.

- Launch an ec2 instance which has MYSQL setup already with security group allowing  port 3306 in private subnet so that our wordpress vm can connect with the same.
Also attach the key with the same.

