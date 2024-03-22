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
}