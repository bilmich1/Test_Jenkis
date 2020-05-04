pipeline {
    agent any
    
    stages {
        stage('build') {
            steps {
                bat "echo %time%"
                bat "ping 127.0.0.1 -n 3"
                bat "echo %time%"
            }
        }
    }
}