pipeline {
    agent any

    stages {
        stage('Copy Docker-compose file') {
            steps {
               sshagent(['prod-credential']) {
                    sh 'scp -o StrictHostKeyChecking=no docker-compose.yml ubuntu@13.229.233.163:/home/ubuntu/docker-compose.yml'
                    sh 'ssh -o StrictHostKeyChecking=no ubuntu@13.229.233.163 docker-compose up -d'
                    }
                    
                }    
            }
   

        
    }
}
