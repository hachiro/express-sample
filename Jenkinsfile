pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            sh 'echo "hello" > hello.txt'
          }
        }
        stage('hello2') {
          steps {
            sh 'echo "hello2"'
          }
        }
      }
    }
    stage('error') {
      steps {
        archiveArtifacts 'hello.txt'
      }
    }
    stage('after_hello') {
      steps {
        sh 'echo "after hello"'
      }
    }
  }
}