pipeline {
  agent any
  stages {
    stage('sonar') {
      steps {
        withSonarQubeEnv 'Sonar'
        waitForQualityGate true
      }
    }
  }
}