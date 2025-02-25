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
                    def files = findFiles(glob: '*.txt')
                    if (files.isEmpty()) {
                        echo "No text files found."
                    } else {
                        for (file in files) {
                            echo "Contents of ${file.name}:"
                            sh "cat ${file.path}"
                        }
                    }
                }
            }
        }
    }
}
