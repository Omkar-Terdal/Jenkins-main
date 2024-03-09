pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o PES1UG22CS825-1 PES1UG22CS825-1.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using a shell script
                    sh './PES1UG22CS825-1'
                }
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
