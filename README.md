<h1> Docker Image Deployment on Amazon ECS Cluster </h1>

Step1 - Set Up an ECS Cluster
- Create an ECS Cluster:
- Open the ECS Management Console and create a new cluster.
Select "Networking only" for Fargate
- Click on create

Step 2 - Create a Task Definition
- Go to ECS Task Definitions:
- Choose Fargate as the launch type.
Configure the Task Definition:
Add a container:
- Set a container name (e.g., my-container).
- Use the ECR image URI (e.g., <account_id>.dkr.ecr.us-east-1.amazonaws.com/my-docker-app).
- Specify port mappings (e.g., 80:80 for HTTP) 0r (e.g., 3000:3000 for React-app)
- Allocate memory and CPU resources.
- Click on create

Step 3 - Run the Service
- Create a Service:
- Use your task definition and set the desired number of tasks.
Set Up Networking:
- Ensure a VPC, subnets, and security groups are available for your cluster.
- Allow inbound HTTP/HTTPS traffic if deploying a web app.
- Launch the Service:
- Deploy the service to your cluster.

Step 4 - Verify the Deployment
- Check Service Status:
- Confirm the service is running in the ECS console.
- Access Your Application:
- Use the public IP or domain name of your ECS service to access the application.

