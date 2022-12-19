
pipeline {
    agent any
 stages {
    stage('old build down') {
            steps {
               sh 'sudo chmod 777 -R /var/jenkins_home/workspace/CICDWORKFLOW/'
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
               sh 'docker compose down'
            }
        }
   
        stage('Git Repo') {
            steps {
                sh 'sudo chmod 777 -R /var/jenkins_home/workspace/CICDWORKFLOW/'
                sh 'rm -R /var/jenkins_home/workspace/CICDWORKFLOW/*'
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
                sh 'composer dump-autoload'
             
            }
        }
        
    stage('Build UP') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
                 sh 'docker compose up -d'
            }
        }
    stage('Testing') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
                 sh 'phpunit --log-junit testinglogs.xml'
            }
        }

    }
}
