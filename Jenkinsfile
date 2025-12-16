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
          docker-compose down --remove-orphans
          docker-compose up -d --build
        '''
    }
}
    }
}

