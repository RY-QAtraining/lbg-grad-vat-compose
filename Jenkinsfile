pipeline{
 environment {
      registryCredentials = "dockerhub_id"
    }
    agent any
  stages{
   stage("checkout"){
     steps{
      script{
      git branch:'main', url: 'https://github.com/RY-QAtraining/lbg-grad-vat-compose.git'
      }}
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
