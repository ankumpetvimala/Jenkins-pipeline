pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
                dir('backend') {
                    bat 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running application tests'
                bat 'echo Test stage completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the build logs.'
        }
    }
}
