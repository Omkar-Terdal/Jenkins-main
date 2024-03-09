pipeline {
    // Use a dedicated agent block with desired executor configuration
    agent any

    stages {
        // Stage for cloning the repository
     //  stage('Clone repository') {
      //      steps {
       //         // Use checkout step with proper configuration
        //        checkout([
         //           $class: 'GitSCM',
           //         branches: [[name: 'main']], // Assuming you want the main branch
             //       userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]
             //   ])
            //}
        //}

        // Stage for building the application
        stage('Build') {
            steps {
                // Use sh for shell commands with proper syntax\
                build 'PES1UG22CS825-1'
                sh 'g++ task5.cpp -o output' // Output filename should be in quotes
            }
        }

        // Stage for testing the application
        stage('Test') {
            steps {
                // Execute the compiled program (assuming output is the executable)
                sh './output'
            }
        }

        // Stage for deployment (add specific deployment commands here)
        stage('Deploy') {
            steps {
                // Replace with actual deployment commands (e.g., scp, rsync)
                echo 'Deployment logic goes here' // Placeholder for deployment steps
            }
        }
    }

    // Post section for handling pipeline failures
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
