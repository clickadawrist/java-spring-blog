pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "hi"
                sh "./mvnw clean install -DskipTests"
            }
        }
        stage("Test") {
            steps {
                sh "./mvnw test"
            }
        }
        stage("Deploy") {
            steps {
                sh "./mvnw clean heroku:deploy"
            }
        }
    }
}
