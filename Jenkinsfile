pipeline {
    agent any
    
    stages {
        stage ('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/varshini400/ci-cd-project'
            }
        }
        stage ('build') {
            steps {
                sh 'docker build -t image1:v1 .'
            }
        }
        stage ('run') {
            steps {
                sh 'docker run -itd -p 8080:80 image1:v1'
            }
        }
    }

}
