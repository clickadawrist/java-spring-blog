pipeline {
    agent any
    pollSCM(cron(* * * * *))
    stages {
        stage("build") {
            steps {
                sh "./mvnw clean install -DskipTests"
            }
        }
        stage("test") {
            steps {
                sh "./mvnw test"
            }
        }
        stage("deploy") {
            steps {
                sh "./mvnw clean heroku:deploy"
            }
        }
    }
}