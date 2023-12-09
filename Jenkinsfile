pipeline {
    agent any
 tools {
        maven 'local_maven'
    }

    stages {
        
        stage('api-gateway') {
            when {
                changeset '**/api-gateway/**'
            }  
            steps {
                 dir('api-gateway') {
                    sh 'mvn clean package'
                }
            }
                
        }
        stage('admin-server') {
            when {
                changeset '**/admin-server/**'
            }  
            steps {
                 dir('admin-server') {
                    sh 'mvn clean package -Dmaven.test.skip=true'

                }
            }
                
        }

        
        }
    }
