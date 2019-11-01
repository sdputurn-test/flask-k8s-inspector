pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'python --version'
                sh "pwd "
                sh "touch abc.txt"
                sh "ls -ltra"
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*.txt', fingerprint: true
        }
    }
}
