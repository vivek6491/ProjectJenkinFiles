pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Release') {
            steps {
                echo "Building production release on master"
                sh 'mvn clean install -DskipTests=true'
            }
        }
    }
    }

