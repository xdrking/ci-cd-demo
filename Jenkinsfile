pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch:'xdrking', url: 'https://github.com/xdrking/ci-cd-demo.git'  // Proje GitHub repo URL'si
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-demo .'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'echo "Running Tests..."'
                // Test komutlarını buraya ekleyebilirsin
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 3000:3000 ci-cd-demo'
            }
        }
    }
}
