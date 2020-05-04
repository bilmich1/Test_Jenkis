pipeline {
    agent any
    
    stages {
        stage('setup') {
            steps {
                bat "echo %time%"
                bat "ping 127.0.0.1 -n 4"
                bat "echo %time%"
            }
        }

        stage('build') {
            steps {
                bat "echo %time%"
                bat "ping 127.0.0.1 -n 4"
                bat "echo %time%"
            }
        }

        stage('test') {
            steps {
                bat "echo %time%"
                bat "ping 127.0.0.1 -n 4"
                bat "echo %time%"
            }
        }

        stage('deploy') {
            steps {
                bat "echo %time%"
                bat "ping 127.0.0.1 -n 4"
                bat "echo %time%"
            }
        }
    }
}