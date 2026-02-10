pipeline {
    agent any
    stages {
        stage('Clean Workspace') {
            steps {
                deleteDir() // deletes all files in the workspace
            }
        }
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Run avg2.py') {
            steps {
                sh 'python app/avg2.py'
            }
        }
    }
}

