pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh './app.sh'
            }
        }

        stage('Test') {
            steps {
                sh './test.sh'
            }
        }

        stage('Package') {
            steps {
                sh '''
                    mkdir -p dist
                    echo "artifact content" > dist/app.txt
                '''
            }
        }
    }

    post {
        success {
            echo "CI pipeline succeeded"
        }
        failure {
            echo "CI pipeline failed"
        }
        always {
            cleanWs()
        }
    }
}

