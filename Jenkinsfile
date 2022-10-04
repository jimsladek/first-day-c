pipeline {
    agent any
    
    stages {
        stage('Build Make') { 
            steps { 
                sh 'make build '
                writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."
            }
        }

    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
    }
}
