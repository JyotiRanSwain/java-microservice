pipeline {
    agent any
 tools {
        maven 'local_maven'
    }

    stages {
        
        stage('api-gateway') {
            steps {
                 dir('api-gateway') {
                    sh 'mvn clean package'
                }
            }
                
        }
        stage('service-one') {
            steps {
                 dir('service-one') {
                    sh 'mvn clean package'
                }
            }
                
        }

        
        }
    }
