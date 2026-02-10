pipeline {
    agent any

    tools {
        git 'git'
    }
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
            agent {
                docker {
                    image 'python:3.10'
                }
            }
            steps {
                sh 'python app/avg2.py'
            }
        }
    }
}

