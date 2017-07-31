pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        parallel(
          "Drone Approved?": {
            milestone 1
            sh 'echo `date`'
            
          },
          "E2E Approved": {
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
          "Deploy": {
            echo 'hello'
            
          },
          "Disable Rotation": {
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