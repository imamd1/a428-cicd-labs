pipeline {
    agent any
    checkout scm
    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
                args '-p 3001:3001'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}