pipeline {
    agent any
    
    stages {
        stage('Download') {
            steps {
                gcc HelloWorld.c > generatedFile.txt'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
    }
}
