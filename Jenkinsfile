pipeline {
    //agent any
    agent { node { label 'workstation1' } }

    environment {
       TEST_URL = "google.com"
       SSH = credentials("centos-ssh")
    }

    stages {
        stage('compile') {
            steps {
                //echo 'Hello World'
                //error 'This is an error'
                echo TEST_URL
                echo SSH
                sh env
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