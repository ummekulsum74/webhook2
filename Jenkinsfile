pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java application'
                bat 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Java application'
                bat 'java Hello'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Java application'
                bat 'java Hello'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully'
        }

        failure {
            echo 'CI Pipeline failed'
        }
    }
}
