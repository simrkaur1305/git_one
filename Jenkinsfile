pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build stage'
      }
    }

    stage('upload') {
      parallel {
        stage('upload') {
          steps {
            echo 'upload'
          }
        }

        stage('warning-check') {
          steps {
            echo 'warning-check'
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