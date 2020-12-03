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
            script {
              catchError(buildResult: 'FAILURE', stageResult: 'FAILURE') {
                sh 'false'
              }
            }

            emailext(subject: 'Warning-check', body: 'warning-check passed', from: 'sandhaysimran@gmail.com', to: 'sandhaysimran@gmail.com', attachmentsPattern: '*.html')
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