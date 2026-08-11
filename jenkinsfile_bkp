pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.8.2/bin:$PATH"
    }
    stages {
        stage("clone code"){
            steps{
               git 'https://github.com/vikky100cc/hello-world.git'
            }
        }
        stage("build code"){
            steps{
              sh "mvn clean install"
            }
        }
    }
}
