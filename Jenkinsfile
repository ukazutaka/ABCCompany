#!/usr/bin/env groovy

pipeline {
    agent {
        docker { 
            image 'hrishioa/oyente' 
            args '-v $CUSTOMERROOT/ABCCompany/:/ABCCompany $NFSROOT:/nfs -w /ABCCompany'
            reuseNode true   
               }
    }
    environment {
        PATH = "/product/project/customers:$PATH"
        CUSTOMERROOT = "/product/project/customers"
        NFSROOT = "/nfs"
    }
    stages {
        stage('Test') {
            steps {
                sh 'python $CUSTOMERROOT/ABCCompany/oyente.py $CUSTOMERROOT/ABCCompany/greeter.sol > /nfs/`date "+%Y%m%d_%H%M%S"`.json'
            }
        }
    }
}
