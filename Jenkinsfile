pipeline {
    //agent any
    agent { node { label 'workstation1' } }

    environment {
       TEST_URL = "google.com"
       SSH = credentials("centos-ssh")
    }

     options {
            ansiColor('xterm')
        }

     parameters {
       string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

       text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

       booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

       choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

       password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')

      }
      //
     triggers { pollSCM('*/1 * * * *') }

    stages {
        stage('compile') {
           //input {
             //message "Should we continue?"
             //ok "Yes, we should."
       // }

        when {
          branch 'production'
           }
            steps {
                //echo 'Hello World'
                //error 'This is an error'
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'ansible -i 18.208.201.110, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
            }
        }

    }
    post {
       always {
          echo 'Post'
          //Send Email
          // Trigger Some other Job
          // Update some JIRA Status about the build.

       }
    }
}
def samplef() {
     print "XYZ FUNCTION"
     }
def x = 10
    env.y = 20

node('workstation1') {

  stage('Test') {
     print x
     sh 'echo y - ${y}'
     samplef
  }
}