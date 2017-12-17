pipeline {
  agent {
    node {
      label 'aliyun'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'date'
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
            node(label: 'aliyun') {
              build 'TestDeployment'
            }
            
          }
        }
      }
    }
  }
}