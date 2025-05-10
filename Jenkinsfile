pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo '''
                 ls -al
                 pwd 
                 echo "Hello, World!"
                '''
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