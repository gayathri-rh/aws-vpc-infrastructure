# Decision Flow

```mermaid
flowchart TD

Start[User sends HTTP request]

Start --> ALB[Application Load Balancer]

ALB --> CheckHealth{Is target healthy?}

CheckHealth -->|Yes| Forward[Forward request to Private EC2]

Forward --> Nginx[Nginx Web Server]

Nginx --> Response[Return HTML response]

Response --> User[User receives webpage]

CheckHealth -->|No| Error[Return error response]
