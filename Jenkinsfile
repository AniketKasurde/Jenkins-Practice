pipeline {

    agent any 

    parameters {
        booleanParam(
            name: 'RUN_TESTS',
            defaultValue: true,
            description: 'Run test stage or skip it'
        )
    }

    stages{
        stage('build'){
            
            steps {
                echo "build stage running"
            }
        }

        stage('tests'){

            when {
                expression {param.RUN_TESTS}
            }

            steps {
                echo "running tests..."
            }
        }
    
    }
}