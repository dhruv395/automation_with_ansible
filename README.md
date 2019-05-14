# automation_with_ansible
automation with ansible in AWS.

  	ec2 – create, terminate, start or stop an instance in ec2:
To create EC2 instances, will use the ec2 module. The ec2 module allows us to perform the below operations on instances :
•	start
•	stop
•	terminate
•	stop

    Create, modify, and terminate AWS virtual private clouds.
VPC and Subnets: create the VPC itself, along with public and private subnets across availability zones.
Internet Gateway: configure a gateway for our public resources to access the internet
NAT Gateway: configure a NAT gateway to allow our private resources to access the public internet
VPC Route Tables: define the routing to make our subnets public or private (route public traffic using either the public or NAT gateway)
Security Groups: define some useful security groups for limiting communication only within the VPC, and/or to allow SSH or HTTP/S traffic from the public internet
 VPC for a 3-tier architecture using  Ansible:
We will create subnets in multiple regions for the following:
	ELB(Public Subnet)
	App Server(Private Subne
	 DB Server(Private Subnet)
Playbook structure will be:
playbook.yml
 inventory
  vars.yml
  roles/
        vpc/
            tasks/
                main.yml
