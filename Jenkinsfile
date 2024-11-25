pipeline {
    agent {
        label "agent-1"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Simulating a build step
                sh 'exit 0' // Simulate success; change to 'exit 1' to test failure
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Simulating a test step
                sh 'exit 0' // Simulate success
            }
        }
        stage('prod'){
            steps{
                sh '''
                  netstat -lntp
                  pwd
                  '''
            }
        }
    }
    post {
        always {
            echo 'Cleaning up resources...'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
        unstable {
            echo 'Pipeline is unstable. Please review warnings.'
        }
        aborted {
            echo 'Pipeline was aborted by the user.'
        }
    }
}
