pipeline {
    agent any
    
    stages {
        stage('git branch') {
            steps {
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
                 sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/ &&  docker-compose up --url /var/jenkins_home/workspace/CICDWORKFLOW/'
            }
        }
    }

}
