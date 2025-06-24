pipeline {
    agent any

triggers {
        githubPush()
    }

    stages {
        stage('Checkout1') {
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
// This is a single-line comment
