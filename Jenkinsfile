pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                echo 'Cloning the Terraform Project from Github'
                git branch: 'main', url: 'https://github.com/clovette/terraform-ec2-demo.git'
            }
        }

        stage('Terraform INIT') {
            steps {
                echo 'Terraform INIT'
                sh 'terraform init'
            }
        }

        stage('Terraform PLAN') {
            steps {
                echo 'Terraform PLAN'
                sh 'terraform plan'
            }
        }
    }
}
