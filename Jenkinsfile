pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                    mkdir -p dist
                    echo "Build output $(date)" > dist/app.txt
                '''
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'dist/**', fingerprint: true
            cleanWs()
        }
    }
}
