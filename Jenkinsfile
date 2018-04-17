pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        sh 'npm install'
        sh 'npm test'
      }
    }
  }
}