pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                // Intentional error: Incorrect file name in the g++ command
                build 'PES2UG21CS322-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echhoo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
