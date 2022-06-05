pipeline {
    agent any

    stages {
        stage('Copy Docker-compose file') {
            steps {
               sshagent(['prod-credential']) {
                    sh 'scp -o StrictHostKeyChecking=no docker-compose.yml ubuntu@13.229.233.163:/home/ubuntu/docker-compose.yml'
                    sh 'ssh -o StrictHostKeyChecking=no ubuntu@13.229.233.163 docker-compose up'
                    }
                    
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
