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
        stage('admin-server') {
            steps {
                 dir('service-one') {
                    sh 'mvn clean package'
                }
            }
                
        }

        
        }
    }
