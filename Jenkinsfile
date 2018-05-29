pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "Hello"'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'build sucees pass'
          }
        }
        stage('platform 1-A') {
          steps {
            sh 'echo "test platform 1A"'
          }
        }
        stage('platform 2-A') {
          steps {
            sh 'echo "platform 2A"'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'deployment successfull'
      }
    }
  }
}