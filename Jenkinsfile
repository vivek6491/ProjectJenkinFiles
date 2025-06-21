pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "Building production artifact"
                sh 'mvn clean install -DskipTests=true'
            }
        }
    }
}

