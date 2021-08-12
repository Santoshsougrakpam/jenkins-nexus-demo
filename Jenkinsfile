pipeline {
  agent any
  stages {
    stage('checkout, build') {
      steps {
        sh '''withCredentials([usernamePassword(
credentialsId: \'nexus-credentials\',
usernameVariable: \'nexusUser\',
passwordVariable: \'nexusPassword\'
)]) {
 ./gradlew clean build
}'''
        }
      }

    }
  }