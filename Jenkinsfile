// DECLARATIVE

pipeline {
    // agent any
    agent { docker { image 'maven:3.6.3'} }
    stages {
        stage('Build') {
            steps {
                sh "mvn --version"
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