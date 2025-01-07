pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }

    stages {
        stage("Maven-Build") {
            steps {
                sh '''
                
                cd my-maven-docker-project
                mvn clean install

                '''
            }
        }

        stage("Docker-Build") {
            steps {
                sh '''
                cd my-maven-docker-project
                docker build -t java-image:v1 .
                '''
                
            }
        }
    }
}