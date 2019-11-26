pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 8000:8000'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './scripts/test.sh' 
            }
        }
    }
}
