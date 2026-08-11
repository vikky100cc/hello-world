pipeline {

    agent any

    stages {
 
        stage('Checkout Info') {

            steps {
               
                echo '=============================='
                sh 'git branch --show-current || true'
                sh 'git log --oneline || true'
                sh 'pwd'
                sh 'ls -la'
                ehco '=============================='
            }

        }    


        stage('Build') {

            steps {

                echo '=============================='          
                echo 'Build stage'
                echo '=============================='            

            }

        }
 
        stage('Test') {

            steps {

                echo '=============================='
                echo 'Test stage' 
                echo '=============================='

            }

        }

    }

    post {

        success {

            echo 'CI pipeine is successful'
        }

        failure {
            
            echo 'CI pipeline failed'

        }

    } 

}
