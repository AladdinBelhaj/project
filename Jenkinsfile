pipeline{
    agent any

    environment{
        DOCKER_IMAGE = 'first-container'
    }

    stages{
        stage('Code Checkout'){
            steps{
                git ''
            }
        }
    }
}