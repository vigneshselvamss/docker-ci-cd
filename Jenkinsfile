
node {
  def app

    stage('Maven Install') {

      checkout scm

      }

    stage('Docker Build') {

         sh '''
         docker build -t webapp .
         '''
       
  }

    stage('Run docker image'){
        
         sh '''
         docker run -d -p 8090:80 webapp
         '''
       

    }
    }
