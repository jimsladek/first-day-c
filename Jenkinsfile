pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                gcc HelloWorld.c
                echo ./hello
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'generatedFile.txt', onlyIfSuccessful: true
        }
     }
}
