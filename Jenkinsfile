pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install') {
            steps {
                bat '"C:\\Users\\Gukes\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat '"C:\\Users\\Gukes\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m pytest -v'
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
