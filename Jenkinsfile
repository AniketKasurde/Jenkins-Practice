pipeline {
    agent any

    parameters {
        choice(
            name: 'ENV',
            choices: ['dev', 'stage', 'prod'],
            description: 'Deployment environment'
        )
    }

    stages {
        stage('Deploy') {
            when {
                expression { params.ENV == 'dev' }
            }
            steps {
                echo "Deploying to DEV environment"
            }
        }
    }
}
