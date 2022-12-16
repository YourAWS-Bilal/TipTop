pipeline {
    agent any
     stages {
        stage('build') {
            steps {
             sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
                 sh 'sudo docker compose up'
            }
        }
    }

}
