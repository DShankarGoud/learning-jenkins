//pipeline {
//  agent {
//    node {
//       label 'ansible'
//    }
//  }
//
//  options {
//     disableConcurrentBuilds()
//     ansiColor('xterm')
//  }
//
 // triggers { cron('*/1 * * * *') }
//  triggers { pollSCM('*/1 * * * *') }
//
//  parameters {
//          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
//          text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
//          booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
//          choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
//          password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
//  }
//
// environment {
//    DEMO_URL = "google.com"
//    SSH = credentials("SSH")
// }
//  stages {
//
//    stage ('Test') {
//      environment {
//        DEMO_URL = "yahoo.com"
//      }
//      steps {
//       echo 'Hello World'
//       echo DEMO_URL
//       echo SSH
//       sh 'echo -e "\\e[31mHello"'
//       echo PERSON
//
//      }
//    }
//
//    stage ('Test1') {
//          steps {
//            echo 'Hello World'
//          }
//    }
//  }
//
//  post {
//    always {
//      echo 'OK'
//    }
//  }
//}
//
//
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
//

pipeline {
  agent any

   tools {
      maven 'maven'
   }

  stages {

    stage('one') {
      input {
        message "Do you approve?"
        ok "YES"
        submitter "admin"
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        }
      }
       steps {
         sh 'echo PERSON' = ${PERSON}
       }
    }
  }

}
