pipeline {
    agent any

    tools {
        nodejs "NodeJS" 
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Aiman-ui/nodejs-jenkins-project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test || echo "Tests failed but continuing..."'
            }
        }

        stage('Node Version') {
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }
    }
}
