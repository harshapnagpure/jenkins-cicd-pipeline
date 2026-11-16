
pipeline {
    agent any

    parameters {
        choice(
            name: 'ENVIRONMENT',
            choices: ['dev', 'qa', 'prod'],
            description: 'Select deployment environment'
        )
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out customer-api source code'
            }
        }

        stage('Build') {
            steps {
                script {
                    def appName = 'customer-api'
                    def appVersion = '1.0.0'

                    echo "Application Name: ${appName}"
                    echo "Application Version: ${appVersion}"
                }
                echo 'Build process started'
                echo 'Build completed successfully (simulated)'
            }
        }

        stage('Test') {
            steps {
                echo 'Application testing started'
                echo 'All tests passed (simulated)'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    def appName = 'customer-api'
                    def environment = params.ENVIRONMENT
                    def appVersion = '1.0.0'

                    echo "Application: ${appName}"
                    echo "Environment: ${environment}"
                    echo "Version: ${appVersion}"

                    if (environment == 'dev') {
                        echo 'Development deployment started'
                    }
                    else if (environment == 'qa') {
                        echo 'QA deployment started'
                    }
                    else if (environment == 'prod') {
                        echo 'Production deployment requires approval'
                    }
                    else {
                        error("Invalid environment: ${environment}")
                    }

                    def environments = ['dev', 'qa', 'prod']

                    environments.each { env ->
                        echo "Processing environment: ${env}"
                    }

                    echo 'Deployment workflow simulation completed'
                }
            }
        }
    }
}

