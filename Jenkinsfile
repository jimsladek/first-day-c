pipeline {
    agent any
    
    stages {
        stage('Build') { 
            steps { 
                sh 'make build '
                writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."

        stage "Archive build output"
           archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'
            }
        }
    }
}
