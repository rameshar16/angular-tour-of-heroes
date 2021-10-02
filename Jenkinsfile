pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
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