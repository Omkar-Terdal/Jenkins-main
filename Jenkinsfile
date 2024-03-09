pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    try {
                        sh 'make build'
                    } catch (Exception e) {
                        currentBuild.result = 'FAILURE'
                        echo "Build failed: ${e.message}"
                        error("Build failed: ${e.message}")
                    }
                }
            }
        }
        // Add additional stages for test and deploy as needed
    }
    
    post {
        always {
            echo "Pipeline completed with result: ${currentBuild.result}"
            if (currentBuild.result == 'FAILURE') {
                echo 'pipeline failed'
            }
        }
    }
}
