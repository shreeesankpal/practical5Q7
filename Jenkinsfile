pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/shreeesankpal/practical5Q7.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t javajenkinsapp:v1 .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --name java_container javajenkinsapp:v1'
            }
        }
    }
}