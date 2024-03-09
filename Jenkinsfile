pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Placeholder: Compile your code here
                echo 'Compiling code...'
            }
        }
        stage('Test') {
            steps {
                // Placeholder: Run tests here
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                // Placeholder: Deploy artifacts here
                error added 
                echo 'Deploying...'
            }
        }
    }
    post {
        always {
            // Display 'pipeline failed' message in case of any errors
            echo 'Pipeline failed'
        }
    }
}
