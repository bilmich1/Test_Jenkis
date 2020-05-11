pipeline {
    agent any
    
    options { 
        timestamps()
    }

    environment {
        STAGE_DURATION = '5';
    }

    stages {
        stage('setup') {
            steps {
                bat "echo before setup"
                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('build') {
            steps {
                bat "echo before build"
                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('test') {
            steps {
                bat "echo before test"
                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('deploy') {
            steps {
                bat "echo before deploy"
                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }
    }

    post {
        always {
            logstashSend failBuild: true, maxLines: -1
        }
    }
}