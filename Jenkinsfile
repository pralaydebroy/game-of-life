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
                slackSend()
            }
        }

    }
}