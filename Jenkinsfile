pipeline {
    agent any

    environment {
        APP_NAME = 'my-app'
    }

    options {
        timestamps()
        timeout(time: 30, unit: 'MINUTES')
    }

    parameters {
        choice(
            name: 'ENV',
            choices: ['dev', 'qa', 'prod'],
            description: 'Choose the Environment'
        )
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Pipeline Build for system info'
                sh 'hostname'
                sh 'whoami'
                sh 'pwd'
                sh 'echo $APP_NAME'
                echo "Selected Environment: ${params.ENV}"
            }
        }
        
        stage('Test') {
            steps {
                script {
                    def status = sh(
                        script: 'date',
                        returnStatus: true
                    )

                    echo "Exit code: ${status}"

                }

            }
 
        }

        stage('Production') {
            when {
                branch 'main'
            }

            steps {
                echo 'Production Deployment'
            }
        }
    }
}

post {

    always {
        echo 'Always Excuted'
    }

    success {
        echo 'Build Success'
    }

    failed {
        echo 'Build Failed'
    }

    aborted {
        echo 'Build Aborted'
    }

}
