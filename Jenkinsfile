pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-nginx-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop my-nginx-container || true'
                sh 'docker rm my-nginx-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name my-nginx-container my-nginx-app'
            }
        }

        stage('Check Running Containers') {
            steps {
                sh 'docker ps'
            }
        }
    }
}
