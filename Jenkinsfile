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
        stage('Deploy') {
              steps {
                 echo 'Deploying'
              }
        }
    }
    post {
        always {
            echo 'Build terminé.'
        }
        success {
            echo 'Build réussi !'
        }
        failure {
            echo 'Build échoué.'
        }
    }

}
