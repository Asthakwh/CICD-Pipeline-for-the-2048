Implemented end-to-end CI/CD pipeline for Dockerized applications using AWS CodePipeline, Amazon ECR, and Amazon ECS.
Source (GitHub)
   ↓
CodePipeline
   ↓
CodeBuild (buildspec.yml)
   ↓
Docker Image Build
   ↓
Amazon ECR (Image Repository)
   ↓
Amazon ECS (Deployment)

How It Works
Developer pushes code to GitHub
CodePipeline triggers automatically
CodeBuild builds Docker image
Image pushed to ECR
ECS service updates with new image
