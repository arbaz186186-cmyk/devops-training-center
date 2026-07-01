pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Hello Arbaz'

                sh 'pwd'
                sh 'ls'
                sh 'whoami'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mywebsite .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name mywebsite-container mywebsite'
            }
        }

    }
}
