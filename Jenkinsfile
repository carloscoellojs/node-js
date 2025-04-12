pipeline {
    agent any
    tools {
        nodejs "node"
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/carloscoellojs/node-js.git'
            }
        }
    }
}