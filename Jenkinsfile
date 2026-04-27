pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-nginx-app:latest .'
            }
        }

        stage('Load Image into Minikube') {
            steps {
                sh 'minikube image load my-nginx-app:latest'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s-deployment.yaml'
            }
        }

        stage('Restart Deployment') {
            steps {
                sh 'kubectl rollout restart deployment my-nginx-deployment'
            }
        }

        stage('Check Pods') {
            steps {
                sh 'kubectl get pods'
            }
        }
    }
}
