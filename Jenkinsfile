pipeline {

    agent any

    stages {
 
        stage('Checkout Info') {

            steps {

                sh 'git branch --show-current || true'
                sh 'git log --oneline || true'
                sh 'pwd'
                sh 'ls -la'
            }

        }    


        stage('Build') {

            steps {
          
                echo 'Build stage'

            }

        }
 
        stage('Test') {

            steps {

                echo 'Test stage' 
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
