pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm install && npm run ng build'
            }
        }
        stage('Start') {
            steps {
                script{
                    withEnv(['JENKINS_NODE_COOKIE=dontKillMe']) {
                        sh "nohup ng serve &"
                    }
                }
            }
        }
    }
}