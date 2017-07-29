pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        parallel(
          "Example": {
            sh 'echo `date`'
            
          },
          "Test": {
            sh '''echo `date`
'''
            
          }
        )
      }
    }
    stage('error') {
      steps {
        parallel(
          "error": {
            echo 'hello'
            
          },
          "bhadri": {
            sh '''echo "hello"
'''
            
          }
        )
      }
    }
    stage('Tet') {
      steps {
        sleep 30
      }
    }
    stage('Done') {
      steps {
        sh 'echo hello'
      }
    }
  }
}