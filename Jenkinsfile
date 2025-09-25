pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t registration:v1 .'
            }
        }
        stage('Push to Docker Hub') {
            steps {
                bat 'docker tag registration:v1 shravani152004/registration:v1'
                bat 'docker push shravani152004/registration:v1'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f C:\Users\Admin\Documents\1285\deployment.yaml'
                bat 'kubectl apply -f C:\Users\Admin\Documents\1285\service.yaml'
            }
        }
    }
}
