#!/usr/bin/env groovy

pipeline {
    agent {
        docker { image 'hrishioa/oyente' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python --version'
            }
        }
    }
}
