pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven 3.6.3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven 3.6.3') {
                    sh 'mvn test'
                     echo 'Testing maven project'
                //ABC indicates the folder name where the pom.xml file resides
                bat ' mvn -f pom.xml clean install' 
                }
            }
        }
    }
}
