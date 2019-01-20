pipeline {
    agent any

    stages {
        stage ('Validate Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn clean validate'
                }
            }
        }
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'MVN_HOME') {
                    sh 'mvn install'
                }
            }
        }
    }
}
