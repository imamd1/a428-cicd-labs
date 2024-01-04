pipeline {
    environment{
        VERCEL_TOKEN=credentials('vercel-token')
        VERCEL_SCOPE='imamd'
    }
    // agent any
    agent {
        docker {
            image 'node:20-alpine'
            // args '-p 3000:3000'
        }
    }
    stages {
        stage('check vercel') {
            steps {
                // sh 'npm i -g vercel'
                sh 'vercel --version'
            }
        }
        // stage('Build') {
        //     steps {
        //         sh 'rm -rf node_modules/ && rm -rf package-lock.json'
        //         sh 'npm install'
        //         sh 'sudo npm i -g vercel'
        //         sh 'vercel --token ${VERCEL_TOKEN}'
        //         sh 'vercel --version'
        //     }
        // }
        // stage('Test') {
        //     steps {
        //         sh './jenkins/scripts/test.sh'
        //     }
        // }
        // stage('Deploy') {
        //     steps {
        //         sh './jenkins/scripts/deliver.sh'
        //         input message: 'Sudah selesai menggunakan React App? (Klik "Proceed" untuk mengakhiri)'
        //         sh './jenkins/scripts/kill.sh'

        //     }
        // }
    }
}
