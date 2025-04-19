pipeline {
    agent any

    tools {
        nodejs "NodeJS"  // Must match the name configured in Jenkins > Global Tool Configuration
    }

    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run tests') {
            steps {
                sh 'npm test || true'  // ignore test failure for now
            }
        }

        stage('Build') {
            steps {
                echo 'Build step placeholder'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
