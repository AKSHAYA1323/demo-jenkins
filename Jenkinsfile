pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'docker build -t demo-jenkins .'
            }
        }

        stage('Show Images') {
            steps {
                bat 'docker images'
            }
        }
        stage('Push'){
            steps{
                bat 'docker push demo-jenkins'
            }
        }
    }
}