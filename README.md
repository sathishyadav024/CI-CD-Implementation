# DEVELOPMENT OF CI/CD IN AWS USING:
 SOURCE AS : CODECOMMIT

 BUILD AS  : CODEBUILD

 DEPLOY AS : ELASTICBEANSTALK


# Created a Git repository Using CodeCommit

repo name : sathishrepo3

Clone Url : https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/sathishrepo3

added the files:

.ebextensions

app.py

buildspec.yaml

requirements.txt

Commited the files:

Git commit -m " added the app.py , requirements.txt , .ebextensions and buildspec.yml files "

used "git push origin main" to push the changes to central repository

codecommit image : ![alt text](<Screenshot 2024-04-21 182138-1.png>)

# ELASTICBEANSTALK :

The elasticbeanstalk is works as a platform as a service

Elastic Beanstalk is a service for deploying and scaling web applications and services. Upload your code and Elastic Beanstalk automatically handles the deployment—from capacity provisioning, load balancing, and auto scaling to application health monitoring.

Elastic Beanstalk image : ![alt text](<Screenshot 2024-04-21 173619.png>)

Click on the create application

Environment Creation : ![alt text](<Screenshot 2024-04-21 173715.png>)

Give the application name and configure the environment

Check the availability of domain because it should be unique

Image : ![alt text](<Screenshot 2024-04-21 173818-1.png>)

Select application code as sample application

set the ec2 virtual machine as single instance(free-tier-eligible)

Image : ![alt text](<Screenshot 2024-04-21 173914.png>)

Configure the service access :

Give the service role for the elasticbeanstalk

Give the keypair for the ec2-instance

Create and Give the ec2-instance-profile for the elasticbeanstalk to access the ec2

Next enter the option Skip to review because we don't need any other services for this project

Image : ![alt text](<Screenshot 2024-04-21 174019.png>)

Than click on the submit button

Image : ![alt text](<Screenshot 2024-04-21 174153.png>)

The environment creation is started

Image : ![alt text](<Screenshot 2024-04-21 174402.png>)

The Environment is successfully created

![alt text](<Screenshot 2024-04-21 174510.png>)
![alt text](<Screenshot 2024-04-21 174526.png>)

# CODEPIPELINE

Now go to the codepipeline and click on the Create Pipeline

Image : ![alt text](<Screenshot 2024-04-21 174651.png>)

Give the pipeline name, select the pipeline-type and execution-mode

Image : ![alt text](<Screenshot 2024-04-21 174903.png>)

# SOURCE

Click on Create a new-service-role

than click on next option

Image : ![alt text](<Screenshot 2024-04-21 174925.png>)

# CODEBUILD

Give the provider name as codebuild

Select the region

Image : ![alt text](<Screenshot 2024-04-21 175118.png>)

Click on the create project

Select the build environment details

Image : ![alt text](<Screenshot 2024-04-21 175303-2.png>)
 
Select the details regarding the operating system and the runtime

create the new-service role

Image : ![alt text](<Screenshot 2024-04-21 175321.png>)

Enter the buildspec.yaml file name in the build specifications

Image : ![alt text](<Screenshot 2024-04-21 175343.png>)

select the cloudwatch for logs and click on the continue to the codepipeline

than click on next to go to deploy stage

Image : ![alt text](<Screenshot 2024-04-21 175353.png>)

# DEPLOY

Select the ElsticBeanstalk as deployer in deploy provider

Select the application name and environment name you have created in the elastic beanstalk and click on next to create the pipeline

The pipeline is created

Image : ![alt text](<Screenshot 2024-04-21 175449.png>)

The source stage is successfully succeeded

The Build stage is successfully succeeded

Image : ![alt text](<Screenshot 2024-04-21 181612.png>)

The deploy stage is Successfully Executed

Image : ![alt text](<Screenshot 2024-04-21 181627.png>)

The Environment is successfully updated in&by the elasticbeanstalk

Image : ![alt text](<Screenshot 2024-04-21 181520.png>)

The Application is Successfully Deployed in the Production Level and made Available for the users

Due to the Autoscaling and loadbalancing features of elasticbeanstalk the application works continuously and consistensly

Image : ![alt text](<Screenshot 2024-04-21 181554.png>)

# The Project Is Completed Successfully


