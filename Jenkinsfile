pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        sh 'npm install'
        sh 'npm test'
        sh 'npm start'
        input(message: 'Finished?', ok: 'Yes')
        sh 'sudo fuser -k 1337/tcp'
        echo 'Process killed!'
      }
    }
  }
}