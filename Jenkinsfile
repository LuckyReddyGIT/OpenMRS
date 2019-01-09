pipeline {
    agent any 
    stages {
        stage('Clone repo and clean it') {
            steps {
                sh "git clone https://github.com/openmrs/openmrs-contrib-android-client.git"
                sh "mvn clean -f openmrs-contrib-android-client"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test -f openmrs-contrib-android-client"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package -f openmrs-contrib-android-client"
            }
        }
    }
}
