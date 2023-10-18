pipeline {
    agent any
 tools {
        maven 'local_maven'
    }

    stages {
        
        stage('Build and Test') {
            parallel {
                stage('admin-server') {
                    steps {
                        dir('admin-server') {
                            sh 'mvn clean package'
                            // You can add more Maven-related build and test commands as needed
                        }
                                    post {
                success {
                    echo 'Archiving the artifacts'
                    archiveArtifacts artifacts: '**/target/*.jar'
                }
            }
                    }
                }

                stage('api-gateway') {
                    steps {
                        dir('api-gateway') {
                            sh 'mvn clean package'
                            // You can add more Maven-related build and test commands as needed
                        }
                                    post {
                success {
                    echo 'Archiving the artifacts'
                    archiveArtifacts artifacts: '**/target/*.jar'
                }
            }
                    }
                }
            }
        }

        
        }
    }
