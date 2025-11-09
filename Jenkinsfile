pipeline {
    agent {
        docker {
            image 'node:24.11.0-alpine3.22'
            args '-v /c/Users/User/.jenkins/workspace:/workspace -w /workspace'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
            }
        }
    }
}
