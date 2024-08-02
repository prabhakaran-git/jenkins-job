pipeline {
    agent any
    
    parameters {
        string(name: 'GREETING', defaultValue: 'Hello', description: 'Greeting message')
        choice(name: 'ENVIRONMENT', choices: ['DEV', 'QA', 'PROD'], description: 'Environment to deploy')
        booleanParam(name: 'DEBUG', defaultValue: true, description: 'Enable debug mode')
    }

    stages {
        stage('Print Parameters') {
            steps {
                script {
                    echo "Greeting: ${params.GREETING}"
                    echo "Environment: ${params.ENVIRONMENT}"
                    echo "Debug mode: ${params.DEBUG}"
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    if (params.ENVIRONMENT == 'DEV') {
                        echo "Building for Development environment"
                        // Add build steps for DEV environment
                    } else if (params.ENVIRONMENT == 'QA') {
                        echo "Building for QA environment"
                        // Add build steps for QA environment
                    } else if (params.ENVIRONMENT == 'PROD') {
                        echo "Building for Production environment"
                        // Add build steps for PROD environment
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
                // Add deploy steps here
            }
        }
    }
}
