pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Elvi-2202/depotgithub.git'
            }
        }

         stage('install docker') {
            steps {
                  sh 'sudo apt-get update'
                  sh 'sudo apt-get install apt-transport-https  ca-certificates curl software-properties-common -y'
                  sh 'sudo apt-get install docker.io -y'
                  sh 'sudo apt update'
                  sh 'sudo chmod 666 /var/run/docker.sock'
                  sh 'sudo usermod -aG  docker $USER'
                  sh 'sudo systemctl restart docker.service'
            }
        }
    }
} 
