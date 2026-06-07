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
         stage('Run') {
            steps {
                bat 'docker run --rm akshaya494/demo-jenkins'
            }
        }
        stage('Push') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'dockerhub',
                        usernameVariable: 'DOCKER_USER',
                        passwordVariable: 'DOCKER_PASS'
                    )
                ]) {
                    bat 'docker login -u %DOCKER_USER% -p %DOCKER_PASS%'
                    bat 'docker push akshaya494/demo-jenkins'
                } 
            }
        }  

    }
}