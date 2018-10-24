#!/usr/bin/env groovy

pipeline {
    agent {
        docker { 
            image 'hrishioa/oyente' 
            args '-v /product/project/customers/ABCCompany/:/ABCCompany -w /ABCCompany'
            reuseNode true   
               }
    }
    stages {
        stage('Test') {
            steps {
                sh 'python oyente.py greeter.sol'
            }
        }
    }
}
