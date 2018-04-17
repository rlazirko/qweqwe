pipeline {
  agent any
  stages {
    stage('NPM Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Run') {
      steps {
        sh 'pm2 start app.js'
      }
    }
    stage('Turn off') {
      steps {
        input 'Enough?'
        sh 'pm2 stop app'
      }
    }
  }
}