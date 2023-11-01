// DECLARATIVE

pipeline {
    agent any
    // agent {
    //     docker {
    //         image 'maven:3.6.3'
    //     }
    // }
    stages {
        stage('Build') {
            steps {
                sh "mvn --version"
                echo "Build"
                echo "$PATH"
                echo "$BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "$JOB_NAME - $env.JOB_NAME"
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
