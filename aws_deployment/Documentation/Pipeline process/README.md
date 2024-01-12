# Pipeline process
> Please refer to the included pipeline diagram titled ```pipeline.png``` in the root of this file to further illustrate the flow of the pipeline.  

## CircleCI
I used CircleCI for CI/CD automation of this project. The project was linked to my personal GitHub repo: https://github.com/0mar-aly/udagram  
The pipeline works as follows: 
- A new commit is made to the linked GitHub repo.
- The CircleCI workflow is triggered.
- The workflow sets up the environment as specified in the ```config.yml``` file, installing the required orbs.
- The jobs are then executed one by one to build and deploy the project to AWS.  
### Job steps
The workflow runs scripts from the project-level ```package.json``` file, which are:
- Spin up a Docker container.
- Install the required orbs.
- Run ```npm install``` in both the API and the frontend folders.
- Run the respective build scripts for the API and the frontend.
- Run the respective test scripts for the API and the frontend.
- Run the commands in both ```deploy.sh``` file, which run in the AWS CLI and EB CLI. Deploying both the frontend and the backend to AWS.

### Orbs used
> All mentioned orbs can be found on: https://circleci.com/developer/orbs
- circleci/node@5.0.2
- circleci/aws-cli@1.4.1
- circleci/aws-elastic-beanstalk@2.0.1
- circleci/browser-tools@1.2.5

### CircleCI badge
> [![0mar-aly](https://circleci.com/gh/0mar-aly/udagram.svg?style=svg)](https://app.circleci.com/pipelines/github/0mar-aly/udagram)  
I also included screenshots showing the CircleCI project status in the Screenshots folder in the root of this submission.
## Environment Variables and configuration 
**No Environment variables or authentication strings are present in the source code**.  
The environment variables and AWS access keys were passed to CircleCI, and then I passed the CircleCI environment variables to the deployment environment using ```eb setenv``` in the Elastic Beanstalk CLI.  
> Example:  
> ```eb setenv POSTGRES_USERNAME=$POSTGRES_USERNAME POSTGRES_PASSWORD=$POSTGRES_PASSWORD POSTGRES_DB=$POSTGRES_DB DB_PORT=$DB_PORT ```  
A screenshot of the environment variables in my CircleCI is included in this folder.  
  
The config file (titled ```config.ts```) was updated to refer to the environment variables in the source code. Note that the source code is available on my repo linked in the section above.  

## Accessing the application
To access the app, please visit http://udagram-test-bucket.s3-website-us-east-1.amazonaws.com/  
> Note: You may need to disable CORS (Cross origin resource Sharing), to do so, please refer to this Stack Overflow answer explaining so using Google Chrome: https://stackoverflow.com/a/6083677