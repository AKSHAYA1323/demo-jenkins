pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'docker build -t akshaya494/demo-jenkins .'
            }
        }

        stage('Show Images') {
            steps {
                bat 'docker images'
            }
        }
        stage('Push'){
            steps{
                bat 'docker push akshaya494/demo-jenkins'
            }
        }
    }
}