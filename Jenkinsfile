pipeline{
    agent any

    environment{
        DOCKER_IMAGE = 'first-container'
    }

    stages{
        stage('Code Checkout'){
            steps{
                git 'https://github.com/AladdinBelhaj/project'
            }
        }

        stage('Deploy Docker with Docker Compose'){
            steps{
                sh 'docker-compose up --build'
            }
        }
    }
}