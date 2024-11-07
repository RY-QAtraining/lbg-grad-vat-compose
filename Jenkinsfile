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
      }
     }
   }
    stage('run '){
     steps{
      script{
       sh 'ssh jenkins@35.210.188.186 docker.withRegistry('',registryCredentials){
       docker compose -f ./lbg-grad-vat-compose/docker-compose.yaml up -d --build}' 
      }
  }
}
}
}
