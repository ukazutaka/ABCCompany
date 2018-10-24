#!/usr/bin/env groovy

pipeline {
    agent {
        docker { image 'hrishioa/oyente' }
    }
    stages {
        stage('Test') {
            steps {
                python 'oyente.py greeter.sol'
            }
        }
    }
}
