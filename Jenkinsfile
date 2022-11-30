pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' //test trigger
            }
        }
      stage('unit tests') {
            steps {
              sh "mvn test"
            }
        }   
    }
}
