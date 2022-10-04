pipeline {
    agent any
    
    stages {
        stage('Build') { 
            steps { 
                sh 'make' > generatedFile.txt'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
    }
}
