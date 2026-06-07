pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/AKSHAYA1323/demo-jenkins.git'
            }
        }
        stage('Build'){
            steps{
                bat 'docker build -t demo-jenkins .'
            }
        }
        stage('show docker images'){
            steps{
                bat 'docker images'
            }
        }
    }
}