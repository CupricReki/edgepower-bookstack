pipeline {
  agent any
  stages {
    stage('Build docker container') {
      steps {
        sh 'docker build . -t edgepower-bookstacks'
      }
    }
    stage('Deploy docker') {
      steps {
        sh 'docker compose up'
      }
    }
  }
}