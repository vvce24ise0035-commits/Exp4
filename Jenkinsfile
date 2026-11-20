
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
                echo 'Building Java application'
                bat 'javac app.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Executing Java application tests'
                bat 'java app'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Java application'
                bat 'java app'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline completed successfully'
        }

        failure {
            echo 'CI pipeline failed'
        }
    }
}
