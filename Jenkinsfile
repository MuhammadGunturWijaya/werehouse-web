pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Ihsanuddin18/werehouse-web.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                sh 'composer install'  // Jika menggunakan PHP & Laravel
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'php artisan test'  // Jalankan unit test Laravel (sesuaikan jika pakai framework lain)
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
                // Contoh deploy ke server, bisa pakai SCP atau rsync
                sh 'scp -r . user@your-server:/var/www/html'
            }
        }
    }
}
