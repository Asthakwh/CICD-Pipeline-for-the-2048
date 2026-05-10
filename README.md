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
1=Developer pushes code to GitHub
2=CodePipeline triggers automatically
3=CodeBuild builds Docker image
4=Image pushed to ECR
5=ECS service updates with new image

Download docker
install AWS cli

      AWS configure
create cluster in ECR

      git clone https://github.com/Asthakwh/repo-name
      ls
      cd CICD-Pipeline-ecs/
      docker build .
      docker run -d -p 80:80 --name CICD-ecs-app 2e367659a0b8
      docker ps
      aws ecr get-login-password --region ap-south-1 | docker login --username AWS --password-stdin 024239493672.dkr.ecr.ap-south-1.amazonaws.com/myappnew
      
      docker tag 2e367659a0b8 123456789012.dkr.ecr.ap-south-1.amazonaws.com/CICD-ecs-app:latest
      docker push 024239493672.dkr.ecr.ap-south-1.amazonaws.com/myappnew:latest

