pipeline {
  agent any
  stages {
  stage('src') {
      steps {
        git(url: 'https://github.com/gargmunish/jenkins', branch: 'master')
      }
    }
    stage('Sonar') {
      parallel {
        stage('Sonar') {
          steps {
            sh '''hello
'''
          }
        }
        stage('PMD') {
          steps {
            sh '''none
'''
          }
        }
        stage('Check Style') {
          steps {
            sh '## Add Check style here'
          }
        }
      }
    }
    stage('Build Business Service') {
      parallel {
        stage('Build-BusinessService') {
          steps {
            sh 'mvn clean install'
          }
        }
        stage('Build Data Service') {
          steps {
            sh 'mvn clean install'
          }
        }
      }
    }
    stage('Deploy to Dev') {
      steps {
        sh '## add Test here'
      }
    }
    stage('Unit Test') {
      steps {
        sh '## Add Test Step here'
      }
    }
    stage('Deploy to Release') {
      steps {
        sh '## Deploy to release'
      }
    }
    stage('Functional Test') {
      steps {
        sh '# Add functional Test'
      }
    }
    stage('Deploy to Stage') {
      steps {
        sh '# Deploy to Stage box'
      }
    }
    stage('Performance Test') {
      parallel {
        stage('Performance Test') {
          steps {
            sh '## Add Lisa Test'
          }
        }
        stage('UAT Test') {
          steps {
            sh '## Add Lisa Test'
          }
        }
      }
    }
    stage('Deploy to Prod') {
      steps {
        sh '## Add prod to Deploy'
      }
    }
  }
}
