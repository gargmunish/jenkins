pipeline {
  agent any
  stages {
    stage('Git Lab Check Out ') {
      steps {
        git(url: 'https://github.com/gargmunish/jenkins', branch: 'master', changelog: true, credentialsId: 'gitLabcredetials')
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean'
        sh 'mvn install'
      }
    }
  }
}