pipeline {
  agent any
  tools {
    git 'Default'
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build & Deploy') {
      steps {
        script {
          sh 'docker-compose up -d --build'
        }
      }
    }
  }
}
