pipeline {
    agent {
        label "agent-1"
    }

    stages {
        stage('build-2') {
            steps {
                sh " echo this is build"
            }
        }
        stage ("test-2"){
            steps{
                sh " echo this code-test"

            }
        }
        stage("deploy-2"){
            steps{
                sh "echo this code-test"
            }
        }
        stage("prod"){
            steps{
                sh "echo this prod"
            }
        }
    }
    post {
        always {
            echo "this section run always"
            deletedir()
        }
        success{
            echo " this jenkins file is successs"
        }
        faliure{
            echo " this jenkins file is failure"
        }
    }
}