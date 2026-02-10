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
        stage('Run avg.py') {
            steps {
                sh 'python version2/app/avg2.py'
            }
        }
    }
}

