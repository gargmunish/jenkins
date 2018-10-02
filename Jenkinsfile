pipeline {
  agent any
  stages {
    stage('Sonar') {
      parallel {
        stage('Sonar') {
          steps {
            sh '''echo "Add sonar settings here"
'''
          }
        }
        stage('PMD') {
          steps {
            sh '''echo "Add PMD settings here"
'''
          }
        }
        stage('Check Style') {
          steps {
            sh 'echo "Add checkstyle settings here"'
          }
        }
      }
    }
    stage('Build Business Service') {
      parallel {
        stage('Build-BusinessService') {
          steps {
            sh 'echo "mvn clean install"'
          }
        }
        stage('Build Data Service') {
          steps {
            sh 'echo "mvn clean install"'
          }
        }
      }
    }
    stage('Deploy to Dev') {
      steps {
        sh 'echo "Deploy settings here"'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'echo "Add sonar settings here"'
      }
    }
    stage('Deploy to Release') {
      steps {
        sh 'echo "Add sonar settings here"'
      }
    }
    stage('Functional Test') {
      steps {
        sh 'echo "Add sonar funtional test settings here"'
      }
    }
    stage('Deploy to Stage') {
      steps {
        sh 'echo "Add sonar settings here"'
      }
    }
    stage('Performance Test') {
      parallel {
        stage('Performance Test') {
          steps {
            sh 'echo "Add sonar settings here"'
          }
        }
        stage('UAT Test') {
          steps {
            sh 'echo "Add sonar settings here"'
          }
        }
      }
    }
    stage('Deploy to Prod') {
      steps {
        sh 'echo "Add sonar settings here"'
      }
    }
  }
}
