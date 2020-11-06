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
                sh 'docker build -t vicky12345/webapp:latest .'
            }
        }
        stage('Docker run') {
            steps {
                sh 'docker run -d -p 8090:80 webapp:latest'
            }
        }  
    }
 }
