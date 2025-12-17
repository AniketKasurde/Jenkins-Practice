pipeline {
    agent any

    stages {
        stage('Create file') {
            steps {
                sh '''
                    echo "This is a temp file" > temp.txt
                    ls -l
                '''
            }
        }

        stage('Force failure') {
            steps {
                sh 'exit 1'
            }
        }
    }

    post {
        always {
            echo 'Cleaning workspace...'
            cleanWs()
        }
    }
}

