# Architecture Diagram

```mermaid
flowchart TB

User[User Browser]

subgraph AWS VPC
    ALB[Application Load Balancer]

    subgraph Public Subnet
        Bastion[Bastion Host EC2]
    end

    subgraph Private Subnet
        App[Private EC2 Instance<br>Nginx Web Server]
    end
end

User -->|HTTP Request| ALB
ALB -->|Forward Port 80| App

Admin[DevOps Engineer] -->|SSH| Bastion
Bastion -->|SSH| App
