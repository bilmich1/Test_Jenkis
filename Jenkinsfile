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
                    echo "start stage setup"
                }

                bat "ping 127.0.0.1 -n 2"
                
                logstash {
                    echo "end stage setup"
                }
            }
        }

        stage('build') {
            steps {
                logstash {
                     echo "start stage build"
                }

                bat "ping 127.0.0.1 -n 8"
                
                logstash {
                     echo "end stage build"
                }
            }
        }

        stage('test') {
            steps {
                logstash {
                     echo "start stage test"
                }

                bat "ping 127.0.0.1 -n 10"
                
                logstash {
                     echo "end stage test"
                }
            }
        }

        stage('deploy') {
            steps {
                logstash {
                     echo "start stage deploy"
                }

                bat "ping 127.0.0.1 -n 5"
                
                logstash {
                     echo "end stage deploy"
                }
            }
        }
    }

    post {
        always {
            logstash {
                echo "end of build"
            }
        }
    }
}