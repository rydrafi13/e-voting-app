pipeline {
    agent any

    stages {
        stage('Pull Source Code') {
            steps {
                git branch: 'main', url: 'https://github.com/rydrafi13/e-voting-app.git'
            }
        }
        stage('Build Container Image') {
            steps {
                sh 'docker compose build'
            }
        }
        stage('Deploy Container Apps') {
            steps {
                sh 'docker compose up -d'
            }
        }
        stage('Push Image') {
            steps {
                sh 'docker compose push'
            }
        }
    }
}
