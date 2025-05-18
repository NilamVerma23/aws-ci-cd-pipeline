# Python App CI/CD Pipeline using AWS CodePipeline & CodeBuild
This project demonstrates a simple but complete Continuous Integration (CI) pipeline built on AWS.

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
├── app/
│   ├── Dockerfile
│   ├── app.py
│   └── requirements.txt
├── buildspec.yml
└── README.md

Policies attached in role created:-

AmazonSSMFullAccess
AWSCodeBuildAdminAccess
AWSCodePipeline_FullAccess
AWSCodeStarFullAccess
CodeBuildBasePolicy-aws-ci-cd-role-ap-south-1
CodeBuildCodeConnectionsSourceCredentialsPolicy-aws-ci-cd-python-project-ap-south-1-520334513362
ROSAKMSProviderPolicy
SecretsManagerReadWrite
