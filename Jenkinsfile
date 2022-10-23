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
             tomcatDeploy('54.146.160.160','app','Tomcat_server')

            }
        }
    }
}
