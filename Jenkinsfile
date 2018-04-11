pipeline {
  agent any
  stages {
    stage('build') {
       steps {
            echo 'hello world' 
             }
    }
    stage('syncbuild') {
       steps {            
           bat(script: 'echo "hello"', encoding: 'utf-8', returnStatus: true, returnStdout: true)
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
