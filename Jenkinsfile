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
            sh 'false'
            emailext(subject: 'Warning-check', body: 'warning-check passed', from: 'sandhaysimran@gmail.com', to: 'sandhaysimran@gmail.com')
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