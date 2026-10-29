
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'pwd'
                sh 'ls -la'
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
