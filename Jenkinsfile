pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'whoami'
                sh 'rm -rf node_modules'
                sh 'npm install -g @angular/cli && ng --version'
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