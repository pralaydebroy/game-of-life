#!/usr/bin/groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                mvn clean install
            }
        }

    }
}