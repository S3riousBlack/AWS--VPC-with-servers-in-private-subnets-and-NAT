Project:

Design and configure a VPC: Create a VPC with custom IP ranges. Set up public and private subnets. Configure route tables and associate subnets.

Implement network security: Set up network access control lists (ACLs) to control inbound and outbound traffic. Configure security groups for EC2 instances to allow specific ports and protocols.

Provision EC2 instances: Launch EC2 instances in both the public and private subnets. Configure security groups for the instances to allow necessary traffic. Create and assign IAM roles to the instances with appropriate permissions.

Networking and routing: Set up an internet gateway to allow internet access for instances in the public subnet. Configure NAT gateway or NAT instance to enable outbound internet access for instances in the private subnet. Create appropriate route tables and associate them with the subnets.

SSH key pair and access control: Generate an SSH key pair and securely store the private key. Configure the instances to allow SSH access only with the generated key pair. Implement IAM policies and roles to control access and permissions to AWS resources.

Test and validate the setup: SSH into the EC2 instances using the private key and verify connectivity. Test network connectivity between instances in different subnets. Validate security group rules and network ACL settings.



Overview:

The VPC has public subnets and private subnets in two Availability Zones. 
Each public subnet contains a NAT gateway and a load balancer node. 
The servers run in the private subnets, are launched and terminated by using an 
Auto Scaling group, and receive traffic from the load balancer. 
The servers can connect to the internet by using the NAT gateway. ![Uploading image.png…]()


Commands used for this project
ssh- keypair ubuntu@ipaddress
scp command to copy keypair from local machine to bastion
command - scp -i /home/umarkhan/Downloads/keypair1.pem /home/umarkhan/Downloads/keypair1.pem ubuntu@ipaddress: /home/ubuntu
vim index.html
python3 -m http.server 8000
netstat -lntp | grep :8000
sudo kill -9 processid
