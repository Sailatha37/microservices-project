pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                echo "Building Docker Image..."
            }
        }

        stage('Push to DockerHub') {
            steps {
                echo "Pushing image to DockerHub..."
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                echo "Deploying to Kubernetes..."
            }
        }

    }
}