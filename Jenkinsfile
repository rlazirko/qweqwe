pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        sh 'npm install'
        sh 'npm test'
        sh 'pm2 start app.js'
        input(message: 'Finished?', ok: 'Yes')
        sh 'fuser -k 1337/tcp'
        echo 'Process killed!'
      }
    }
  }
}