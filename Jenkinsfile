pipeline {
    stages {
        stage ('Clean workspace') {
            steps {
                cleanWs()
            }
        }

        stage ('Git Checkout') {
            steps {
            git branch: 'main', credentialsId: '', url: 'https://github.com/syuraj/DotNet-test-app.git'
            }
        }

        stage('Build') {
            steps {
            bat "dotnet build --configuration Release"
            }
        }
    }
}
