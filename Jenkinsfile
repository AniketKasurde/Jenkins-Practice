pipeline {
    agent any

    parameters {
        string(
            name: 'APP_VERSION',
            defaultValue: '1.0.0',
            description: 'Application version to build'
        )
    }

    stages {
        stage('Show Version') {
            steps {
                echo "Building version: ${params.APP_VERSION}"
            }
        }
    }
}
