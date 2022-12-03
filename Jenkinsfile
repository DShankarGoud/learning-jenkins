pipeline {
  agent {
    node {
       label 'ansible'
    }
  }

  options {
     disable ConcurrentBuilds()
     ansiColor('xterm')
  }

 environment {
    DEMO_URL = "google.com"
    SSH = credentials("SSH")
 }
  stages {

    stage ('Test') {
      environment {
        DEMO_URL = "yahoo.com"
      }
      steps {
       echo 'Hello World'
       echo DEMO_URL
       echo SSH
       sh 'echo -e "\\e[31mHello"'

      }
    }

    stage ('Test1') {
          steps {
            echo 'Hello World'
          }
    }
  }

  post {
    always {
      echo 'OK'
    }
  }
}


//node {
//
// stage('Test') {
//   echo 'Hello World'
// }
//
// stage('Test1') {
//   echo 'HelloWorld'
// }
//
//}