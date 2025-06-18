pipeline {
  agent any
  tools {
    git 'Default'
  }
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/enginestop/ntx-devops-test.git'
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
