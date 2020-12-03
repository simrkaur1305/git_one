pipeline {
    agent any
    stages {
        stage('Auto-Build') {
            agent { node {
                    label "master"
                    }
            }
            stages {
                parallel{
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
        }
    }
}
