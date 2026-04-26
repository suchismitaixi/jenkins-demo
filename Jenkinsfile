pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

                sh 'echo "Building application"'

                sh 'pwd'
            }
        }

        stage('Test') {

            steps {

                sh 'echo "Running tests"'

                sh 'date'
            }
        }

        stage('Deploy') {

            steps {

                sh 'echo "Deploying application"'
            }
        }
    }
}
