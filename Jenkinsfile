pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Ihsanuddin18/werehouse-web.git'
            }
        }
        stage('Build') {
            steps {
                echo "Building the application..."
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
}
