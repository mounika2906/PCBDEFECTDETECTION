# PCBDEFECTDETECTION
"PCB defect detection is the process of identifying and diagnosing defects or abnormalities in printed circuit boards to ensure their proper functioning."

![pcb image.png]()

###Software and Tools Requirements

  1.[GithubAccount](https://github.com/)

  2.[VsCodeIDE](https://code.visualstudio.com/)

  3.[AWS](https://aws.amazon.com/)
  
  4.[GitCLI](https://git-scm.com/)


create a new environment

...

conda create -p venv python==3.9 -y

...

## workflows

1. constants
2. entity
3. components
4. pipelines
5. app.py


## documents

  1.[HLD](https://docs.google.com/document/d/1OS3zzAG1LO1a07mIAmsM9C_qeLKqbcPq/edit?usp=sharing&ouid=110561493789800648225&rtpof=true&sd=true)
  
  2.[LLD](https://docs.google.com/document/d/1wmQfv0crz9z-KijJJ4ERBJ08BUUUA0PD/edit?usp=sharing&ouid=110561493789800648225&rtpof=true&sd=true)
  
  3.[Demo Video](https://drive.google.com/file/d/1-ibVkFwmwXlTjuxB7NLigjc5gFJZlsfG/view?usp=sharing)
  
  4.[linkdin post](https://www.linkedin.com/posts/mounika-avadutha-3592731aa_pcbprinted-circuit-board-fault-detection-activity-7127870306966278144-GoPO?utm_source=share&utm_medium=member_desktop)
  
  5.[ppt](https://docs.google.com/presentation/d/1ItuVg0Lj_wDuIsszKcjCL0ypCAGTsyF2/edit?usp=sharing&ouid=110561493789800648225&rtpof=true&sd=true)

  6.[Certificate](https://drive.google.com/file/d/1L3KTVhYwQTBp0PLIKHOeMGeIyLV8giZU/view?usp=sharing)


## install the requirements
```bash
pip install -r requirements.txt
``````
Finally run the following command

```bash
python app.py
``````
Now,

open up you local host and port

# AWS-CICD-Deployment-with-Github-Actions
##  Login to AWS console.
##  Create IAM user for deployment
```bash
##with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
``````

# Create ECR repo to store/save docker image
```bash
- Save the URI: 932166928499.dkr.ecr.eu-north-1.amazonaws.com/defects
``````
## Create EC2 machine (Ubuntu)
## Open EC2 and Install docker in EC2 Machine:
```bash
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
``````

# Configure EC2 as self-hosted runner:
```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
``````
# Setup github secrets:
```bash
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com/defect

ECR_REPOSITORY_NAME = defect
``````



