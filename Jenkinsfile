pipeline {
 agent { node { label 'AGENT-1' } }
  options {
        ansiColor('xterm')
        // timeout(time: 1, unit: 'HOURS')

    } 
      environment { 
        user = 'Aslam'
    }

    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                ls -ltr
                pwd
                echo 'push from git hub 2nd time '
                printenv
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
              //  error 'this is failed '
            }
        }
    }     
    post { 
        always { 
            echo 'I will always whether the job is success or not '
        }
   
  
        success { 
            echo 'I will always when job is success'
        }
        // failure { 
        //     echo 'I will run only when job is faiure'
    
        // }

     }
}