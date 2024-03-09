pipeline {
  agent {
    docker {
      image 'node:14'
    }
  }
  stages {
    stage('Clone repository') {
      steps {
        git branch: 'main',
        url: 'https://github.com/Omkar-Terdal/Jenkins-main.git'
      }
    }
    stage('Install dependencies') {
      // Assuming no dependencies for this example, remove if needed
      // steps {
      //   sh 'npm install'  // Replace with your actual dependency installation command
      // }
    }
    stage('Build application') {
      steps {
        script {
          // Compile the .cpp file using a shell script
          sh """
          # Assuming your .cpp file is named main.cpp
          g++ task5.cpp -o PES1UG22CS825-1  # Replace with your actual .cpp filename
          """
          if (shExitCode != 0) {
            error 'Compilation failed!'
          }
        }
      }
    }
    stage('Test application') {
      steps {
        script {
          // Print the output of the compiled program using a shell script
          sh """
          ./YOUR_SRN-1  # Replace with your actual executable filename
          """
        }
      }
    }
    stage('Push Docker image') {
      // Assuming no Docker image building for this example, remove if needed
      // steps {
      //   sh 'docker build -t <user>/<image>:$BUILD_NUMBER.'
      //   sh 'docker push <user>/<image>:$BUILD_NUMBER'
      // }
    }
  }
}
