pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/kandarisailatha/microservices-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t kandarisailatha/user-service ./user-service'
            }
        }

        stage('Push to DockerHub') {
            steps {
                sh 'docker push kandarisailatha/user-service'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f kubernetes/'
            }
        }
    }
}