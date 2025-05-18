# Python App CI/CD Pipeline using AWS CodePipeline & CodeBuild
This project demonstrates how to implement a CI using AWS CodePipeline, AWS CodeBuild, and DockerHub for a Python application. The source code is managed on GitHub, and the application is containerized using Docker.

# Tech Stack
- AWS CodePipeline – Manages the CI pipeline
- AWS CodeBuild – Builds the Docker image and runs test scripts
- DockerHub – Stores the built image
- GitHub – Source control
- Python – Language used for the app

# CI Flow
1. Developer pushes code to the GitHub repository.
2. AWS CodePipeline detects the changes automatically.
3. AWS CodeBuild:
   - Builds a Docker image using `Dockerfile`
   - Runs tests and/or packaging
   - Pushes Docker image to a container registry

# Project Structure
aws-ci-cd-pipeline/
<br>
├── app/ 
<br>
│   ├── app.py
<br>
│   ├── Dockerfile
<br>
│   ├── requirements.txt
<br>
├── images/
<br>
│   ├── Codebuild Status - Successful.png
<br>
│   ├── Continuous Integration Process.png
<br>
│   ├── Dockerhub.png
<br>
│   ├── Executions in CodePipeline.png
<br>
│   └── Phase details of CodeBuild.png
<br>
├── buildspec.yml
<br>
└── README.md

Policies attached in role created:-
<br>
AmazonSSMFullAccess
<br>
AWSCodeBuildAdminAccess
<br>
AWSCodePipeline_FullAccess
<br>
AWSCodeStarFullAccess
<br>
CodeBuildBasePolicy-aws-ci-cd-role-ap-south-1
<br>
CodeBuildCodeConnectionsSourceCredentialsPolicy-aws-ci-cd-python-project-ap-south-1-520334513362
<br>
ROSAKMSProviderPolicy
<br>
SecretsManagerReadWrite

