pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sailatha/product-service ./product-service'
            }
        }

        stage('Push to DockerHub') {
            steps {
                sh 'docker push sailatha/product-service'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f kubernetes/'
            }
        }

    }
}