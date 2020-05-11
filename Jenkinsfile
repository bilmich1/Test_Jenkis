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
                logstash {
                    bat "echo start stage setup"
                }

                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                
                logstash {
                    bat "echo end stage setup"
                }
            }
        }

        stage('build') {
            steps {
                logstash {
                    bat "echo start stage build"
                }

                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                
                logstash {
                    bat "echo end stage build"
                }
            }
        }

        stage('test') {
            steps {
                logstash {
                    bat "echo start stage test"
                }

                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                
                logstash {
                    bat "echo end stage test"
                }
            }
        }

        stage('deploy') {
            steps {
                logstash {
                    bat "echo start stage deploy"
                }

                bat "ping 127.0.0.1 -n ${STAGE_DURATION}"
                
                logstash {
                    bat "echo end stage deploy"
                }
            }
        }
    }
}