pipeline {
    agent any
    stages {
        stage('Clean') {
            steps {
                sh "mvn clean"
            }
        }

        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }

        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Newman') {
            steps {
                sh "newman run mindicador.cl.postman_collectionJD.json"
            }
        }
    }
}
