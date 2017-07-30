pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        parallel(
          "Example": {
            milestone 1
            sh 'echo `date`'
            
          },
          "Test": {
            milestone 2
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
