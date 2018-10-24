#!/usr/bin/env groovy

pipeline {
    agent {
        docker { image 'mythril/myth' }
        args  '--entrypoint=\'\''
    }
    stages {
        stage('Test') {
            steps {
                sh 'myth --help'
            }
        }
    }
}
