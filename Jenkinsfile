pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/enginestop/ntx-devops-test.git'
      }
    }
    stage('Build & Deploy') {
      steps {
        script {
          sh 'docker-compose down --remove-orphans'
          sh 'docker-compose up -d --build'
        }
      }
    }
  }
}
