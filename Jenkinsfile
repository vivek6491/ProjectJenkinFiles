pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
	triggers {
        githubPush()
    }

        stage('Build Release') {
            steps {
                echo "Building production release on master"
                sh 'mvn clean install -DskipTests=true'
            }
	stage('Build Test') {
            steps {
                echo "Building production release on master"
                sh 'mvn test'
            }
        }
    }
    }
}
