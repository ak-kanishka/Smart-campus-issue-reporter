pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Maven Clean') {
            steps {
                bat 'mvn clean'
            }
        }

        stage('Maven Package') {
            steps {
                bat 'mvn package'
            }
        }

        stage('Verify Files') {
            steps {
                bat 'dir'
            }
        }
    }

    post {
        success {
            echo 'Smart Campus Issue Reporter - Build Successful!'
        }

        failure {
            echo 'Smart Campus Issue Reporter - Build Failed!'
        }
    }
}