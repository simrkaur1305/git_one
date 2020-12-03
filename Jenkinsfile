pipeline {
  agent any
  stages {
    stage('Build') {
      stages {
        stage('warning-check') {
          steps {
            echo 'warning-check'
          }
        }
        stage('validator') {
          steps {
            echo 'validator'
          }
        }
      }
    }
    
    stage('upload') {
        steps {
          echo 'upload'
        }
      }
  }
}
