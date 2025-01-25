
![Architecture Flow of AWS drawio](https://github.com/user-attachments/assets/ac1a56cc-07f7-4d20-8410-84fc624bd5a9)


## Architecture Components and Flow:

User Access: The user accesses the application via a domain (e.g., medochealth.in).<br>  
CloudFront: CloudFront serves static content from the S3 bucket.<br>  
S3 Bucket: Stores static assets like frontend files (HTML, CSS, JavaScript) and media.<br>  
Application Load Balancer (ALB): Handles dynamic content and forwards requests to the EC2 instances.<br>  
EC2 Instances: Host the backend application logic and process API calls.<br>  
Maria DB: Acts as the database for backend operations.<br>  


**# Detail Components and Flow:**

CloudFront (CDN):
Delivers your website's static files (like HTML, CSS, JavaScript) quickly to users worldwide.
Handles user requests and forwards them to the backend services when needed.

Elastic Load Balancer (ELB):
Shares incoming traffic evenly across backend servers (EC2 instances).
Ensures no single server is overloaded.

EC2 Instances (Backend):
Runs the backend application that processes user requests and handles business logic.
Connects to the database to store or retrieve data.

S3 Bucket:
Stores all the website’s static files, like images and code for the frontend.
Works with CloudFront to deliver these files faster to users.

RDS (Relational Database Service):
Stores important structured data, like user details, billing information, or inventory records.

ElastiCache:
Speeds up the application by storing frequently used data temporarily so the database doesn’t have to work as hard.

CloudWatch (Monitoring):
Tracks how well your resources (like EC2, RDS, and ElastiCache) are performing.
Keeps logs of activities, sends alerts if something goes wrong, and shows live performance data in dashboards.



