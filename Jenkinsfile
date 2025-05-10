pipeline {
    agent any
    // options {
    //     // Timeout counter starts AFTER agent is allocated
    //     timeout(time: 1, unit: 'SECONDS')
    // }
    
    stages {
         
        stage ('Example ENV') {
            environment {
                SERVICE_CREDS = credintials('service-creds')

                steps {
                    sh '''
                    echo "service user is $SERVICE_CREDS_USERNAME"
                    echo "service password is $SERVICE_CREDS_PASSWORD"

                    '''
                    echo "example stage"
                }
                
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
                echo "got push form the webhookksss"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
        always {
            echo 'This will always run'
        }
    }
}