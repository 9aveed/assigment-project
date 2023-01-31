pipeline {
    agent {
        any {
            image 'docker:stable-dind'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Build and Push Docker Image') {
            steps {
                sh 'docker login -u navid12 -p naveedalam321'
                sh 'docker-compose build'
                sh 'docker-compose push'
            }
        }
    }
}
