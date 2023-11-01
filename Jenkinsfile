// DECLARATIVE

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Build"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
            }
        }
    } 
    post {
        always {
            echo "declarative message shows always"
        }
        success {
            echo "shows only when build is successful"
        }
        failure {
            echo "shows only when build is failure"
        }
    }
}