pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                gcc -o hello HelloWorld.c
                echo ./hello
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
            junit 'build/reports/**/*.xml'
        }
    }
}
