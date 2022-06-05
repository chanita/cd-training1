pipeline {
    agent any

    stages {
        stage('confirm version') {
            steps {
                nodejs('NodeJS 18.3.0') {
                    sh 'node -v'
                    sh 'npm -v'
                }
            }
        }
        stage('install node packages') {
            steps {
                nodejs('NodeJS 18.3.0') {
                    sh 'npm install'
                }
            }
        }
    }
}
