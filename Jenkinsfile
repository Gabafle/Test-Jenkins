pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
    post {
        always {
            echo 'Build terminé.'
        }
        success {
            echo ' Build réussi !',
             mail to: 'gabriel.peter@edu.devinci.fr',
                         subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
                         body: "Good with ${env.BUILD_URL}"
        }
        failure {
            echo 'Build échoué.',
             mail to: 'gabriel.peter@edu.devinci.fr',
                         subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
                         body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
}
