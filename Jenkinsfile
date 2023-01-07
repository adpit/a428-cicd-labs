node {
    stage('Build') {
        // commands to build the project go here
        docker.image('node:lts-bullseye-slim').inside {
        checkout scm
        sh 'npm install'
        }
    }
    stage('Test') {
        // commands to run tests go here
        docker.image('node:lts-bullseye-slim').inside {
        checkout scm
        sh './jenkins/scripts/test.sh'
        }
    }
    stage('Deploy') {
        // commands to deploy the built project go here
    }
 }