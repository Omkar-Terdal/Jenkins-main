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
        stage('Deploy') {
            steps {
                script {
                    // Add deployment steps here if needed
                    echo 'Deployment not implemented yet'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'pipeline failed'
            // Add any actions to take on failure
        }
    }
}
