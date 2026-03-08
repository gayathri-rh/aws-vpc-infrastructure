# AWS VPC DevOps Project

This project demonstrates a production-style AWS networking architecture using a bastion host and private EC2 instance behind an Application Load Balancer.

## Architecture

Internet -> Application Load Balancer -> Private EC2 (Nginx Web Server) <- Bastion Host (SSH Access)

## Components Used

- AWS VPC
- Public Subnet
- Private Subnet
- Bastion Host
- Private EC2 Instance
- Nginx Web Server
- Application Load Balancer
- Target Group
- Security Groups

## Application Output

The application displays:

"This webpage is hosted on a Private EC2 Instance
inside an AWS VPC and served through an
Application Load Balancer."

This confirms that traffic flows correctly:

## Screenshots

See the `screenshots` folder for infrastructure and application proof.
