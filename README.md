
# Continuous integration and continuous Delivery of a Multi-tier Cloud-native Web application on AWS with Advance Monitoring Capabilities using Prometheus

A simple employee directory web application built with ReactJS for the frontend and NodeJS for the backend logic. It features a Postgres database for storing employee credentials. The application demonstrates my in-depth knowledge of continuous integration and continuous delivery (CICD) by building an automated CICD pipeline using CircleCI to build the linted and properly tested code into a Docker image and deploying it to a development environment on AWS, with the help of Ansible for configuration management and Prometheus and Alert Manager for enhancing the monitoring capabilities of the infrastructure.

## Built With
- [CircleCI](https://circleci.com/) - Cloud-based CI/CD service
- [Amazon AWS](https://aws.amazon.com/) - Cloud services
- [AWS CLI](https://aws.amazon.com/cli/) - Command-line tool for AWS
- [CloudFormation](https://aws.amazon.com/cloudformation/) - Infrastructure as code
- [Ansible](https://www.ansible.com/) - Configuration management tool
- [Prometheus](https://prometheus.io/) - Monitoring tool

## Prerequisites
- [AWS CLI](https://aws.amazon.com/cli/) - Command-line tool for AWS
- [Docker](https://www.docker.com/) - Containerization platform
- [Node.js](https://nodejs.org/) - JavaScript runtime
- [Postgres](https://www.postgresql.org/) - Open-source relational database

## Installation
1. Clone the repository

2. Install the dependencies

   cd employee-directory

   npm install


3. Build the Docker image

    docker build -t employee-directory .
 

4. Run the Docker container


   docker run -p 3000:3000 employee-directory
   

5. Access the application in your browser at http://localhost:3000

## Deployment
1. Login to your AWS account, Create an IAM user with Programmatic access permissions and configure the AWS CLI

2. Create a CloudFormation stack using the provided template
   
   aws cloudformation create-stack --stack-name employee-directory --template-body file://infrastructure.yml

3. Use Ansible to configure the EC2 instances
    
    ansible-playbook -i inventory.ini deploy.yml

4. Deploy the application to the development environment


## Monitoring
1. Access Prometheus at http://<your_ec2_instance_ip>:9090

2. Access Alert Manager at http://<your_ec2_instance_ip>:9093

## Authors

* **Uviekugbere Theophilus** - [Github](https://github.com/CloudKnightOps)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details




[License](LICENSE.md)
