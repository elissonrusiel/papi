pipeline {
    agent {
        dockerfile true  
    }
    stages {
        stage('Build') {
            steps {
                sh 'mkdir build'
                sh 'cd build'
                sh 'cmake ..'
                sh 'make'
            }
        }
        stage('Test') {
            steps {
                sh 'cd build'
                sh 'make test'
            }
        }
        stage('Install') {
            steps {
                sh 'cd build'
                sh 'make install'
            }
        }
    }
}