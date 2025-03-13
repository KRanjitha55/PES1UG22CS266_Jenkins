pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ hello.cpp -o hello.out'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello.out'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
