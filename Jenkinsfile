pipeline {
  agent any
  stages {
    stage('checkout, build') {
      steps {
        withCredentials(bindings: [usernamePassword(credentialsId: 'nexus-credentials', usernameVariable: 'nexusUser',passwordVariable: 'nexusPassword')]) {
          sh '''echo $nexusUser $nexusPassword
./gradlew clean build'''
        }

      }
    }

  }
}