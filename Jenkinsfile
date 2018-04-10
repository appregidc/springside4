pipeline {
  agent {
    node {
      label 'epkf'
    }
    
  }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'hello world'
            timeout(time: 160, unit: 'MINUTES') {
              sh 'echo "hello"'
            }
            
          }
        }
        stage('syncbuild') {
          steps {
            node(label: 'master') {
              bat(script: 'echo "hello"', encoding: 'utf-8', returnStatus: true, returnStdout: true)
            }
            
          }
        }
      }
    }
    stage('Delpoy') {
      steps {
        echo 'done'
      }
    }
  }
  environment {
    env1 = 'dev'
  }
}