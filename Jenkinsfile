
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/saiteja9027-debug/first-proj.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage started'
                sh 'ls -la'
                sh 'cat README.md'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage completed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
