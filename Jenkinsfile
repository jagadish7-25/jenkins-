pipeline {
    agent {
        label "agent-1"
    }

    stages {
        stage('build-1') {
            steps {
                sh " echo this is build"
            }
        }
        stage ("test"){
            steps{
                sh " echo this code-test"

            }
        }
        stage("deploy"){
            steps{
                sh "echo this code-test"
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