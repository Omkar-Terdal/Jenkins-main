pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add commands to build your project here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add commands to test your project here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add commands to deploy your project here
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded'
            // Add any actions to take on successful completion
        }
        failure {
            echo 'Pipeline failed'
            // Add any actions to take on failure
        }
    }
}
