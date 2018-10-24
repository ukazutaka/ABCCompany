#!/usr/bin/env groovy

pipeline {
    agent {
        docker { image 'mythril/myth' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'myth --help'
            }
        }
    }
}
