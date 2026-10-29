
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
                sh 'mvn clean package'
            }
        }

        stage('Verify Artifact') {
            steps {
                sh 'ls -lh target/'
                sh 'test -f target/jenkins-cicd-java-app-1.0.0.jar'
            }
        }
    }

    post {
        success {
            echo 'Java application built successfully!'
        }
        failure {
            echo 'Build failed. Check Console Output.'
        }
    }
}
