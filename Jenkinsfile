#!/usr/bin/env groovy

pipeline {
    agent {
        docker { image 'mythril/myth' }
                dockerfile {
            args '--entrypoint=\'\''
                }
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'myth --help'
            }
        }
    }
}
