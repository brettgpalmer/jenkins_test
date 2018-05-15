@Library('sharedLibrary')

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
                echo "${env.NODE_VER}"
                sh 'curl www.palmersoftware.com'
            }
        }

        stage('Deployment stage') { agent any
            steps {
                echo "Should deploy at this step"
            }
        }

        stage('Parallel') { agent any
            failFast true
            steps {
                parallel(
                  a: {
                    echo "This is branch a"
                  },
                  b: {
                    echo "This is branch b"
                  }
                )
            }
        }



    }

}