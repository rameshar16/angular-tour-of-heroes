pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'sudo npm install -g @angular/cli && sudo npm install -g @angular-devkit/build-angular && ng --version'
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