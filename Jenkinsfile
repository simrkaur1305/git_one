pipeline {
    agent any
    stages {
        agent { node {
                label "master"
                }
        }
        stage('Build') {
            steps {
                echo "build"
            }
        }
        stage('warning-check') {
            steps {
                echo "warning-check"
            }
        }
        stage('Upload') {
            steps {
                echo "upload"
            }
        }
        stage('validator') {
            steps {
                echo "validator"
            }
        }
    }
}
