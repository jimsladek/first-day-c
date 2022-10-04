pipeline {
    agent any
    
    stages {
        stage('Download') {
            steps {
                make > generatedFile.txt
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
    }
}
