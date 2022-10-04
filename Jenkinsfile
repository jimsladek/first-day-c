pipeline {
    agent any
    
    stages {
        stage('Build Make') { 
            steps { 
                sh 'make build '
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
    }
}
