pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Build Backend Image') {
            steps {
                sh 'docker build -t backend-image backend'
            }
        }

        stage('Run NGINX') {
            steps {
                sh 'docker run -d -p 9090:80 nginx'
            }
        }
    }
}