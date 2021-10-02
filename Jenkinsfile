pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'whoami'
                sh 'rm -rf node_modules package-lock.json'
                sh 'npm install'
                sh 'ng build'
            }
        }
        stage('Start') {
            steps {
                sh 'ng serve'
            }
        }
    }
}