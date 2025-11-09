pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'echo "FROM node:20-alpine" > Dockerfile'
                sh 'docker build -t simple-node .'
            }
        }
    }
}
