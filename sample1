pipeline {
    agent {
        docker {
            image 'node:14'
            reuseNode true
        }
    }
    stages {
        stage('Clone repository') {
            steps {
                checkout scm
            }
        }
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build application') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Test application') {
            steps {
                sh 'npm test'
            }
        }
        stage('Push Docker image') {
            steps {
                script {
                    def dockerImage = 'pes1ug22cs825omkarterdal/jenkins'
                    def dockerImageTag = "${dockerImage}:$BUILD_NUMBER"
                    docker.build(dockerImageTag)
                    docker.withRegistry('https://index.docker.io/v1/', 'dockerhubcredentials') {
                        dockerImage.push()
                    }
                }
            }
        }
    }
}
