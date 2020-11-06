pipeline {
    agent any
    stages {
        stage('scm') {
            steps {
                checkout scm
            }
        }
        stage('Docker-Build') {
            steps {
                sh 'sudo docker build -t webapp:latest .'
                sh 'sudo docker push vicky12345/webapp:latest'
            }
        }
        stage('Docker run') {
            steps {
                sh 'sudo docker run -d -p 8090:80 webapp:latest'
            }
        }  
    }
 }
