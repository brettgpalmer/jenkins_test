pipeline {
    agent none
    environment {
        NODE_VER = '8.1.0'
    }
    stages {
        stage('Beginning') { agent any
            environment {
                NEW_VAR = 'Howdy Brett'
            }
            steps {
                echo 'Hello world with update from Brett'
                //use the shell
                sh 'echo $NODE_VER'
                //Drop to grooy and read environment variable
                echo "${env.NEW_VAR}"

            }
        }

        stage('Who ami I?') { agent any
            steps {
                echo "${env.NEW_VAR}"
                sh 'curl www.palmersoftware.com'
            }
        }

    }

}