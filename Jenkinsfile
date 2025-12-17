pipeline {
    agent any

    stages {
        stage('Identify Branch') {
            steps {
                echo "Running on branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Build') {
            steps {
                echo 'Build runs on all branches'
            }
        }

        stage('Dev Only') {
            when {
                branch 'dev'
            }
            steps {
                echo 'This runs only on dev'
            }
        }

        stage('Main Only') {
            when {
                branch 'main'
            }
            steps {
                echo 'This runs only on main'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
