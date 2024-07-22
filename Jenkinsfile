pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    docker.image('composer:latest').inside {
                        sh 'composer install'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                // Your build steps go here
                echo 'Building...'
            }
        }
    }
}
