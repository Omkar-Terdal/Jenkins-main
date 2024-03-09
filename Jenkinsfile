pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o task5 task5.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using a shell script
                    sh './task5'
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
