@Library("shared-lib") _
pipeline {
    agent any
    stages {
        stage ('compile') {
            steps {

                // Run Maven on a Unix agent.
                 sh 'mvn package'
            }
        }

        stage ('deploy') {

            steps {
             tomcatDeploy('172.156.2.3','app','Tomcat-server')

            }
        }
    }
}
