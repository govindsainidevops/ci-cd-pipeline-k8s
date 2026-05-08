pipeline {
    agent any

    environment {
        DOCKER_IMAGE = "govindsaini442/devops-app"
    }

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/govindsainidevops/ci-cd-pipeline-k8s.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }

        stage('Push to DockerHub') {
            steps {
                withCredentials([string(credentialsId: 'dockerhub-password', variable: 'DOCKER_PASS')]) {
                    sh 'echo $DOCKER_PASS | docker login -u your-dockerhub-username --password-stdin'
                    sh 'docker push $DOCKER_IMAGE'
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s-deployment.yaml'
            }
        }
    }
}