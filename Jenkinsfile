pipeline {
    agent any
    options {
		timeout(time: 60, unit: 'MINUTES') //Aborted the pipeline if it takes more than 5 hours
		buildDiscarder(logRotator(numToKeepStr: '30')) //Delete the builds older than 30
		disableConcurrentBuilds() // Disable concurrent builds
		timestamps() //Print the timestamps of each setp
	}
    stages {
        // Build stage
        stage('Build') {
            steps {
                // Install required npm modules
                sh 'npm install'
                // Build the modules
                sh 'npm run ng build'
            }
        }
        stage('Start') {
            steps {
                script{
                    withEnv(['JENKINS_NODE_COOKIE=dontKillMe']) {
                        // Run the application in background
                        sh "nohup ng serve &"
                    }
                }
            }
        }
    }
}