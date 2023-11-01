// DECLARATIVE

pipeline {
    agent any
    // agent {
    //     docker {
    //         image 'maven:3.6.3'
    //     }
    // }
    environment {
        dockerHome = tool "myDocker"
        mavenHome = tool "myMaven"
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages {
        stage('Checkout') {
            steps {
                echo "Build"
                sh 'mvn --version'
                sh 'docker --version'
                echo "$PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
            }
        }
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Integration Test') {
            steps {
                sh "mvn failsafe:integration-test failsafe:verify"
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
