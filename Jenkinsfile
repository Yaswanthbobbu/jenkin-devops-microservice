// DECLARATIVE

pipeline {
    agent {
        docker {
            image 'aksnfug/maven-jdk11-gradle:latest'
        }
    }
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
            echo "This message always shows"
        }
        success {
            echo "This message shows only when the build is successful"
        }
        failure {
            echo "This message shows only when the build fails"
        }
    }
}
