pipeline {
  agent {
    docker {
      image 'firasdotcom/myBackend'
    }

  }
  stages {
    stage('install') {
      parallel {
        stage('install') {
          steps {
            sh 'npm install'
          }
        }
        stage('Test') {
          steps {
            sh '''chmod 0777 ./node_modules/.bin/mocha
npm test'''
          }
        }
      }
    }
  }
}