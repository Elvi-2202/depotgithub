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
    }
} 
