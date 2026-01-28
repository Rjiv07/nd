pipeline {
    agent any
    environment {
        IMAGE_NAME = "prozpek/nd"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Rjiv07/nd.git'
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME:latest .'
            }
        }
        stage('Push Image') {
            steps {
                sh 'docker push $IMAGE_NAME:latest'
            }
        }
    }
}
