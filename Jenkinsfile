pipeline {
  agent any
  stages {
    stage('src checkout') {
      steps {
        git(url: 'https://github.com/gargmunish/jenkins', branch: 'Master')
      }
    }
  }
}