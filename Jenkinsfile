pipeline {
    //agent any
    agent { node { label 'workstation1' } }

    environment {
       TEST_URL = "google.com"
    }

    stages {
        stage('compile') {
            steps {
                //echo 'Hello World'
                //error 'This is an error'
                echo TEST_URL
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