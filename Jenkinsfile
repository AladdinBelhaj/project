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
                sh 'docker build -t $DOCKER_IMAGE'
                
            }
        }
    }
        post {
        success {
            echo 'Build and tests succeeded!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
