pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'http://192.168.0.20:31803/LumiEtherResearch/Starter-Repository.git'
            }
        }
        stage('Display Text Files') {
            steps {
                script {
                    def files = findFiles(glob: '*.txt') // Find all .txt files
                    for (file in files) {
                        sh "cat ${file.path}" // Cat each text file
                    }
                }
            }
        }
    }
}
