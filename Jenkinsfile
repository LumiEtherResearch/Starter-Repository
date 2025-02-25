pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'http://192.168.0.20:31803/LumiEtherResearch/Starter-Repository.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building..."' # Replace with your build commands
            }
        }
    }
}
