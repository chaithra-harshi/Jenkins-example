pipeline {
    agent any

    stages {
        stage ('Build Stage') {

            steps {
                withMaven(maven: 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven: 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}