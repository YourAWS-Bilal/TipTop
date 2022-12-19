
pipeline {
    agent any

    stage('build down') {
            steps {
               sh 'cd /var/jenkins_home/workspace/CICDWORKFLOW/'
               sh 'docker compose down'
            }
        }
    stages {
        stage('Git Repo') {
            steps {
                sh 'rm -R /var/jenkins_home/workspace/CICDWORKFLOW/*'
                git branch: 'main', url: 'https://github.com/YourAWS-Bilal/TipTop'
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
