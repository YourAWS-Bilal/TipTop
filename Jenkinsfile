pipeline {
    agent any
    
    stages {
        stage('git branch') {
            steps {
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
                 sh 'docker-compose up -d --url /var/jenkins_home/workspace/CICDWORKFLOW/'
            }
        }
    }
    
    
     stages {
        stage('build') {
            steps {
                 sh 'docker-compose up -d --url /var/jenkins_home/workspace/CICDWORKFLOW/'
            }
        }
    }

}
