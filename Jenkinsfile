pipeline {
    agent any
    
    environment {
        STAGE_DURATION = '5';
    }

    stages {
        stage('setup') {
            steps {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('build') {
            steps {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('test') {
            steps {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
            }
        }

        stage('deploy') {
            steps {
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