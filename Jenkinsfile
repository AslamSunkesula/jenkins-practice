pipeline {
 agent { node { label 'AGENT-1' } } 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
        always { 
            echo 'I will always whether job is success or not '
        }
    }
    post { 
        success { 
            echo 'I will always say Hello again!'
        }
    }
    post { 
        cleanup { 
            echo 'I will clean the job'
        }
    }
    post { 
        failure { 
            echo 'I will always when the job is failure '
        }
    }
}