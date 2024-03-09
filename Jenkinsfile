pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Add build steps here
                sh 'make build'
            }
        }
        stage('Test') {
            steps {
                // Add test steps here
                sh 'make test'
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
                sh 'make deploy'
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
