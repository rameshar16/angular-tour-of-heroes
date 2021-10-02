pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm run ng build'
            }
        }
        stage('Start') {
            steps {
                sh 'ng serve'
            }
        }
    }
}