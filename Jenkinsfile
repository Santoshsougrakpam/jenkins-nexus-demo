pipeline {
  agent any
  stages {
    stage('checkout, build') {
      steps {
        withCredentials([usernamePassword(credentialsId: 'nexus-credentials', usernameVariable: 'nexusUser',passwordVariable: 'nexusPassword')]) {
         ./gradlew clean build
        }
        }
      }

    }
  }