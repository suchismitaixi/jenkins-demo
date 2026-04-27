pipeline {

    agent any

    stages {

        stage('Build Docker Image') {

            steps {

                sh 'docker build -t my-nginx-app .'
            }
        }

        stage('Check Images') {

            steps {

                sh 'docker images'
            }
        }
    }
}
