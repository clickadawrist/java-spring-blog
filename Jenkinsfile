pipeline {
    agent any
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
                    echo "this is where we would deploy to heroku or some other server"
               }
          }
     }
}