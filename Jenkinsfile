pipeline {
  agent {
    node {
      label 'aliyun'
    }
    
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'date'
          }
        }
        stage('error') {
          steps {
            node('aliyun') {
              build 'SampleBuildJob'
            }
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
        stage('error') {
          steps {
            node('aliyun') {
              build 'TestDeployment'
            }
          }
        }
      }
    }
  }
}
