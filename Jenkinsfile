pipeline {
    agent any
    trigger {
        cron('H 4/* 0 0 1-5')
    }
    stage('Clone Git repo') {
        checkout scm
    }
    stage('Docker Build') {
        steps {
            sh 'docker build -t node:.v.$(BUILD_NUMBER) .'
        }
    }     
}
