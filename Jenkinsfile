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
                echo "Building on DEV branch"
                sh 'mvn clean compile'
            }
        }
        stage('Unit Test') {
            steps {
                echo "Running unit tests on DEV"
                sh 'mvn test'
            }
        }
    }
}

