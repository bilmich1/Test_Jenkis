pipeline {
    agent any
    
    stages {
        stage('setup') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n 3"
                }
            }
        }

        stage('build') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n 3"
                }
            }
        }

        stage('test') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n 3"
                }
            }
        }

        stage('deploy') {
            steps {
                logstash {
                    bat "ping 127.0.0.1 -n 3"
                }
            }
        }
    }
}