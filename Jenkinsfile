pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        withCredentials(bindings: [usernamePassword(credentialsId: 'nexus-credentials', usernameVariable: 'nexusUser',passwordVariable: 'nexusPassword')]) {
          sh './gradlew clean build -PnexusUser=$nexusUser -PnexusPassword=$nexusPassword'
        }

      }
    }

  }
}