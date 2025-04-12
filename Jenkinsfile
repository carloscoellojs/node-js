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
        stage('Linting') {
            steps {
                input 'install npm packages? (Click "yes" to continue)'
            }
        }
        stage('NPM Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Linting') {
            steps {
                input 'Build the application? (Click "yes" to continue)'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}