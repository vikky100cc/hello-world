pipeline {

    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout the Git Source Code'
            }
       }

       stage('Build') {
           steps {
               echo 'Build By Using Maven'
           }
       }

       stage('Test') {
           steps {
               echo 'Running Test using junit'
           }
       }

    }

    post {
    
        success {
            echo 'Pipeline Complited Successfully'
        }

        failure {
            ehco 'Pipline Failed'
         
        }
    }

}
