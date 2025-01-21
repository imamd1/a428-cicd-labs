node {
    // Menjalankan agen menggunakan Docker
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {

        stage('Build') {
            // Menginstal dependensi menggunakan npm
            sh 'npm install'
        }

        stage('Test') {
            // Menjalankan skrip test
            sh './jenkins/scripts/test.sh'
        }
    }
}