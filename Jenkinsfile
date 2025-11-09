pipeline {
    agent any
    stages {
        stage('Build Node container') {
            steps {
                bat '''
                docker pull node:24.11.0-alpine3.22
                docker run --rm node:24.11.0-alpine3.22 node --version
                '''
            }
        }
    }
}
