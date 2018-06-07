pipeline {
    agent any
    stage('Clone Git repo') {
        checkout scm
    }
    stage('Docker Build') {
        steps {
            sh 'docker build -t node:.v.$(BUILD_NUMBER) .'
        }
    }     
}
