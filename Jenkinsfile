pipeline {
    //agent any
    agent { node { label 'workstation1' } }


    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
                error 'This is an error'
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