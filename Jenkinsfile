node {
    // Menjalankan agen menggunakan Docker
    docker.image('node:lts-buster-slim').inside('-p 3000:3000') {

        stage('Build') {
            // Menginstal dependensi menggunakan npm
            sh 'npm install'
        }

        stage('Test') {
            // Menjalankan skrip test
            sh './jenkins/scripts/test.sh'
        }
    }


    withDockerContainer(args: '-p 3001:3001', image: 'node:lts-buster-slim') {
    // some block
    stage('Build') {
            // Menginstal dependensi menggunakan npm
            sh 'npm install'
        }
}
}