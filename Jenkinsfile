pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Trishitamaity/CI_CD_Pipeline'
            }
        }

        stage('Build') {
            steps {
                echo "Building application..."
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                if not exist C:\\deploy-demo mkdir C:\\deploy-demo
                copy CI_CD_Example.html C:\\deploy-demo
                '''
            }
        }
    }
}
