#!/usr/bin/groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               bat'''mvn clean install '''
            }
        }
        stage('Notify') {
            steps {
                slackSend message: '${env.JOB_NAME} - ${env.BUILD_NUMBER} ${env.BUILD_STATUS} after ${env.BUILD_TIME} '
            }
        }

    }
}