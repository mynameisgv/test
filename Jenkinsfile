pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        parallel(
          "Example": {
            echo 'Hello World'
            script {
              def browsers = ['chrome', 'firefox']
              for (int i = 0; i < browsers.size(); ++i) {
                echo "Testing the ${browsers[i]} browser"
              }
            }
            
            
          },
          "Test": {
            sh '''echo "Hello"
'''
            
          }
        )
      }
    }
    stage('') {
      steps {
        parallel(
          "": {
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