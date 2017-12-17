pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'date'
          }
        }
        stage('') {
          steps {
            build 'SampleBuildJob'
          }
        }
      }
    }
    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            sh 'date'
          }
        }
        stage('') {
          steps {
            build 'TestDeployment'
          }
        }
      }
    }
  }
}