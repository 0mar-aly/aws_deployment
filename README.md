# AWS Deployment

## Udagram project

The project consists of a backend/API using Node.js, which connects to a PostgreSQL database using Sequelize to store and retrieve data. The API is connected to a frontend written in AngularJS.

> Disclaimer: I did NOT write this project as it was provided by Udacity for the deployment process course. However, some edits had to be made in order for the project to connect successfully to the database and to pass the frontend tests.

The `package.json` files in both the frontend and the API contain the scripts to build, test, and deploy the application. While the project level `package.json` contains shorthand scripts to execute the respective frontend and API scripts from the project level, to simplify the `config.yml` file used for CircleCI.

## CircleCI

- The CircleCI `config.yml` file installs the OS-level required frameworks and CLI tools (Node.js, AWS CLI, Elastic Beanstalk CLI, and Google Chrome for frontend testing).
- Then, it runs the single workflow, which executes the scripts in the project-level `package.json` file to install all dependencies, build, test, and finally deploy both the frontend and the API.
- All environment variables are stored in CircleCI (more on this in the pipeline process section of the documentation).
- This specific CircleCI project is connected to my personal GitHub repo https://github.com/0mar-aly/udagram

## AWS overview

3 Amazon Web Services were used for this project:

- RDS to set up a PostgreSQL database.
- Elastic Beanstalk to run the API code.
- S3 to store the frontend code.

> I included an architecture diagram titled `architecture.png` in the same folder as this README file to further illustrate how the services communicate.  
> I also included screenshots of each Amazon Web Service showing the status of each service in the Screenshots folder in the root of this submission.

### Example - Account creation

1. The user accesses the frontend using this URL: http://udagram-test-bucket.s3-website-us-east-1.amazonaws.com/
2. The required data is entered.
3. The entered data is passed to the backend (passwords are hashed with bcrypt).
4. The backend saves the data to the database running on RDS.
5. On login, the entered account credentials is compared with the ones saved in the database.

## AWS commands

The commands to setup the S3 bucket and Elastic Beanstalk were included in 2 `deploy.sh` files for the frontend and the backend. This files contains the CLI commands to push the build files to a specified S3 bucket, as well as initiate an Elastic Beanstalk environment and call the environment variables from CircleCI, before deploying the files.

The commands were then called in each folder's `package.json` file in the `scripts` section.
