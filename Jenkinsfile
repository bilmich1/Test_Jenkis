pipeline {
    agent any
    
    environment {
        STAGE_DURATION = '5';
    }

    stages {
        stage('setup') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                }
            }
        }

        stage('build') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                }
            }
        }

        stage('test') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                }
            }
        }

        stage('deploy') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                }
            }
        }
    }
}