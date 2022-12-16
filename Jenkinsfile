pipeline {
    agent any
     stages {
        stage('build') {
            steps {
             
                 sh 'docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d --url /var/jenkins_home/workspace/CICDWORKFLOW/'
            }
        }
    }

}
