pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Compile the task5.cpp file
                sh 'g++ -o task5 task5.cpp'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Execute the task5 executable
                sh './task5'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Placeholder: Add commands to deploy your project here
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
