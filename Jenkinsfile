pipeline {

    agent any

    stages {
 
        stage('Checkout Info') {

            steps {
               
                echo '=============================='
                echo 'Webhook triggered by this build'
                sh 'git branch --show-current || true'
                sh 'git log --oneline || true'
                sh 'pwd'
                sh 'ls -la'
                echo '=============================='
            }

        }    


        stage('Build') {

            steps {

                echo '=============================='          
                echo 'Build stage version 2'
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
