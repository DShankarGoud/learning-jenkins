pipeline {
  agent {
    node {
       label 'ansible'
    }
  }

 environment {
    DEMO_URL= "google.com"
 }
  stages {

    stage ('Test') {
      steps {
       echo 'Hello World'
       echo DEMO_URL

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