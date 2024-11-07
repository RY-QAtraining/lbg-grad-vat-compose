pipeline{
 environment {
      registryCredentials = "dockerhub_id"
    }
    agent any
  stages{
    stage('run using docker-compose file'){
      sh "ssh jenkins@35.210.188.186 docker compose up -d -build"
    }
  }
}
