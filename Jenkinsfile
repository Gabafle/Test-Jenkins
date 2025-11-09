pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                bat 'echo "FROM node:20-alpine" > Dockerfile'
                bat 'docker build -t simple-node .'
            }
        }
    }


}
