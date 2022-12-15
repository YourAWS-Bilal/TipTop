pipeline {
    agent any
    
    stages {
        stage('git branch') {
            steps {
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
            }
        }
    }
       stage('build') {
            steps {
                sh 'cd /var/jenkins_home/workspace/CICD-WORKFLOW/'
                 sh 'docker compose up'
            }
}
