pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                dir('request-management-ui') {
                    bat 'npm install'  // Change sh to bat for Windows
                }
            }
        }
        stage('Build') {
            steps {
                dir('request-management-ui') {
                    bat 'npm run build'  // Change sh to bat for Windows
                }
            }
        }
    }
}
