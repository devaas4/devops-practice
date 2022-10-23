@Library("shared-lib") _
pipeline {
    agent any
    stages {
        stage ('compile') {
            steps {

                // Run Maven on a Unix agent.
                 sh 'mvn compile'
            }
        }

        stage ('deploy') {

            steps {
             tomcatDeploy('172.156.2.3','app','Tomcat-server')

            }
        }
    }
}
