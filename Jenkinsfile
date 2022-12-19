
pipeline {
    agent any
 stages {
    stage('build down') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
               sh 'docker compose down'
            }
        }
   
        stage('Git Repo') {
            steps {
                sh 'rm -R /var/jenkins_home/workspace/CICDWORKFLOW/*'
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
                sh 'composer dump-autoload'
            }
        }
        
    stage('Build') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
                 sh 'docker compose up -d'
            }
        }
    stage('Test') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
                 sh 'phpunit --log-junit testinglogs.xml'
            }
        }

    }
}
