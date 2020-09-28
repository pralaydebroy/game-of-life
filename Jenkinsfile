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
                slackSend message: "Build <a href=\\'${BUILD_URL}\\'>${JOB_NAME} #${BUILD_NUMBER}</a> has been built as ${currentBuild.currentResult}. Took ${currentBuild.durationString}. See the <a href=\\'${BUILD_URL}/console\\'>output</a>."
            }
        }

    }
}