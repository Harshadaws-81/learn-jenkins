pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        // Timeout counter starts BEFORE agent is allocated
        timeout(time: 15, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo This is Build'
                //sh "echo sleep 15"
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is Deploy'
            }
        }
    }

    post {
        always{
            echo "This sections runs always"
            deleteDir()
        
        }
        success{
            echo "This section run when pipeline success"
        }
        failure{
            echo "This section run when pipeline failure"
        }
    } 
}