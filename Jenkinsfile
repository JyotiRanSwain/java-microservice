pipeline {
    agent any
 tools {
        maven 'local_maven'
    }
    stages {
        stage('Build and Package WAR') {
            steps {
                script {
                    // You can define an array of projects or applications
                    def applications = ['api-gateway', 'admin-server']

                    for (app in applications) {
                        // Checkout your source code
                        //checkout scm

                        // Build and package the WAR file for the current application
                        sh "mvn clean package -Dapp=${app}"

                        // Publish the WAR file as an artifact
                        //archiveArtifacts artifacts: "**/target/${app}.war", allowEmptyArchive: true
                    }
                }
            }
        }
    }
}
