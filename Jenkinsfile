pipeline {
    agent any
    tools {
        nodejs "node"
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github-cd', url: 'https://github.com/carloscoellojs/node-js.git'
            }
        }
        stage('Continue and install npm packages') {
            steps {
                input 'install npm packages? (Click "proceed" to continue or "abort" to cancel)'
            }
        }
        stage('NPM Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Continue and build the application') {
            steps {
                input 'Build the application? (Click "proceed" to continue or "abort" to cancel)'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}