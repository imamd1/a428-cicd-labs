pipeline {
    environment{
        VERCEL_TOKEN=credentials('vercel-token')
        VERCEL_SCOPE='imamd'
    }
    agent {
        docker {
            image 'node:alpine3.18'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'rm -rf node_modules/ && rm -rf package-lock.json'
                sh 'npm install'
                sh 'vercel --token ${VERCEL_TOKEN}'
                sh 'npm i -g vercel'
                sh 'vercel --version'
            }
        }
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
