
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Backend source code checked out from GitHub'
            }
        }

        stage('Check Node and npm') {
            steps {
                bat 'node --version'
                bat 'npm --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm ci'
            }
        }

        stage('Lint Backend') {
            steps {
                bat 'npm run lint'
            }
        }
    }
}
