pipeline {
    agent any
    tools {
        nodejs nodejs
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}