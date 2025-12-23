pipeline {

    agent any

    stages{

        stage('checkout'){
            steps{
                checkout scm
            }    
        }

        stage('build'){

            steps {
                sh './app.sh'
            }
        }

        stage('Test'){

            steps {
                sh './test.sh'
            }
        }

        stage('Package'){
            
            steps{

                sh '''
                    mkdir -p dist
                    echo "artifact content" > dist/app.txt
                '''
            }
        }
    }

    post {
        success{
            archiveArtifacts artifacts: 'dist/**', fingerprint: true
        }

        always {
            cleansWs()
        }
    }
}