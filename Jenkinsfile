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
    }
}