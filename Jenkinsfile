pipeline {
    agent any
     stages {
        stage('build') {
            steps {
             
                 sh 'docker compose up -d --url /var/jenkins_home/workspace/CICDWORKFLOW/'
            }
        }
    }

}
