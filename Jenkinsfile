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
    }
}