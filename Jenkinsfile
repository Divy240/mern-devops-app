pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/Divy240/mern-devops-app.git'
            }
        }

        stage('Build') {
            steps {
                bat 'docker compose build'
            }
        }

        stage('Run Containers') {
            steps {
                bat 'docker compose up -d'
            }
        }

        stage('Verify') {
            steps {
                bat 'docker ps'
            }
        }
    }
}