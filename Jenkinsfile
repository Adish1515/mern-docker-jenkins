pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

     stage('Build & Deploy with Docker Compose') {
    steps {
        sh '''
          docker-compose -p mern-cicd down --remove-orphans
          docker-compose -p mern-cicd up -d --build
        '''

    }
}
    

