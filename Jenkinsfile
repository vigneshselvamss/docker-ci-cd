
node {
  def app

    stage('Maven Install') {

      checkout scm

      }

    stage('Docker Build') {

        steps {
         sh '''
         docker build -t webapp .
         '''


       }
  }

    stage('Run docker image'){
        steps {
         sh '''
          docker run -d -p 8090:80 webapp
          '''

       }

    }
}
