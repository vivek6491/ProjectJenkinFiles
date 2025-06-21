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
                echo "Building on QA branch"
                sh 'mvn clean package -DskipTests=false'
            }
        }
        stage('Integration Test') {
            steps {
                echo "Running integration tests"
                sh 'mvn verify'
            }
        }
        stage('Static Analysis') {
            steps {
                echo "Running code quality checks"
                sh 'mvn checkstyle:check'
            }
        }
    }
}

