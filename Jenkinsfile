pipeline {
    agent any
 tools {
        maven 'local_maven'
    }

    stages {
        
        stage('api-gateway') {
            steps {
                 dir('api-gateway') {
                    bat 'mvn clean package'
                    //sh 'docker build -t api-gateway:$BUILD_NUMBER .'           
                    echo 'api-gateway Build Image Completed'
                }
            }
                
        }
        stage('admin-server') {
            steps {
                 dir('admin-server') {
                    bat 'mvn clean package'
                    //sh 'docker build -t admin-server:$BUILD_NUMBER .'           
                    //echo 'admin-server Build Image Completed'
                }
            }
                
        }

        
        }
    }
