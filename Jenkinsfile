pipeline {
    agent none
    stages {
        stage('Beginning') { agent any
            steps {
                echo 'Hello world with update from Brett'
            }
        }

        stage('Who ami I?') { agent any
            steps {
                sh 'host -t TEXT pgp.michaelholley.us |awk -F \'"\' \'{print $2}\''
            }
        }

    }

}