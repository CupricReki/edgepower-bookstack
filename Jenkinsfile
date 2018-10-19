pipeline {
  agent any
  stages {
    stage('Build docker container') {
      steps {
        sh '''docker build . -t edgepower-bookstacks
exit 0'''
      }
    }
    stage('Deploy docker') {
      steps {
        sh 'docker-compose up'
      }
    }
    stage('Tests') {
      steps {
        echo 'Somebody should really add some tests here'
      }
    }
    stage('Notification') {
      steps {
        slackSend 'Hey'
      }
    }
  }
}