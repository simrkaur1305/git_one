pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build stage'
      }
      stages {
        stage('warning-check') {
          steps {
            echo 'warning-check'
          }
        }
        stage('upload') {
          steps {
            echo 'upload'
          }
        }
      }
    }
    stage('validator') {
      steps {
        echo 'validator'
      }
    }

  }
}
