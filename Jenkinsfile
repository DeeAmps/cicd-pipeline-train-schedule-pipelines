pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'npm test'
            }
        }
        stage('Archive') {
            steps {
                echo 'Deploying..'
                zip zipFile: 'build.zip', archive: false, dir: 'archive' // zip the build
                archiveArtifacts artifacts: 'build.zip'
            }
        }
    }
}