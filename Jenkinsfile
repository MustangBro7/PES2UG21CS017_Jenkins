pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS017-1'
                sh 'g++ main.cpp -o output '
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            // Display "pipeline failed" if any of the stages fail
            error 'pipeline failed'
        }
    }
}
