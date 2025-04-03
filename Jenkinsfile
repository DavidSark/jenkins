pipeline {
    agent any
    stages {
        stage('Clonage du dépôt') {
            steps {
                git 'https://github.com/user/repository.git'
            }
        }
        stage('Tests unitaires') {
            steps {
                sh 'python -m unittest discover tests'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:latest .'
            }
        }
        stage('Déploiement') {
            steps {
                sh 'docker run -d -p 8000:8000 myapp:latest'
            }
        }
    }
}
