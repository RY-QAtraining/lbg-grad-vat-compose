pipeline{
 environment {
      registryCredentials = "dockerhub_id"
    }
    agent any
  stages{
   stage("checkout"){
    
   }
    stage('run '){
     steps{
      script{
       sh 'docker-compose -f <docker-compose.yml> logs' 
      }
      script{
      sh 'ssh jenkins@35.210.188.186 docker-compose up -d --build'}
    }
  }
}
}
