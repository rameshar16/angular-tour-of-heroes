pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'whoami'
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