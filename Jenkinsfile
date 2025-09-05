pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Swapnil-Kapale/jenkins_starter_swapnil.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Building app...'
                sh 'python3 --version || python --version'
                sh 'python3 app.py || python app.py'
            }
    }
        stage('Test') {
            steps {
                sh 'echo Running tests...'
                sh 'python3 -m unittest test_app.py'
            }
        }
    }
}
