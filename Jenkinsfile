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
                git branch: 'main', url: '/var/jenkins_home/workspace/CICD-WORKFLOW/docker-compose.yml'
            }
}
