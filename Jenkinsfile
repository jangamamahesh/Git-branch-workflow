pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-credentials', url: 'https://github.com/jangamamahesh/Git-branch-workflow.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Example: Run Maven build
                    sh 'mvn clean install'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Example: Run unit tests
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Example: Deploy to server (modify as per your deployment strategy)
                    sh 'mvn deploy'
                }
            }
        }
    }
}

