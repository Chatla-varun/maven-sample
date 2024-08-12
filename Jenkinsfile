pipeline {
    agent any

    tools {
        maven 'Maven 3.x'  // Ensure Maven is installed on the Jenkins server, and the tool name matches this entry
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Run the Maven build command
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run the Maven test command
                    sh 'mvn test'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and tests were successful!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
