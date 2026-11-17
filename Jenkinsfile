pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t harish-app .'
            }
        }

        stage('Remove Old Container') {
            steps {
                sh 'docker rm -f harish-app || true'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d --name harish-app -p 80:80 harish-app'
            }
        }
    }
}
