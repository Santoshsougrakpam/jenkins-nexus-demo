pipeline {
  agent any
  stages {
    stage('checkout, build') {
      steps {
        sh './gradlew clean build'
      }
    }

  }
}