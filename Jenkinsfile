pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the code using Maven...'
                    // Build automation tool: Maven
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running unit tests using JUnit...'
                    echo 'Running integration tests using TestNG...'
                    // Test automation tools: JUnit for unit tests, TestNG for integration tests
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Analyzing code with SonarQube...'
                    // Code analysis tool: SonarQube
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Performing security scan with OWASP ZAP...'
                    // Security scan tool: OWASP ZAP
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying application to AWS EC2 staging server...'
                    // Deployment target: AWS EC2
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running integration tests on staging environment...'
                    // Integration tests in staging environment
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying application to AWS EC2 production server...'
                    // Deployment target: AWS EC2
                }
            }
        }
    }

    post {
        success {
            emailext(
                subject: 'Pipeline Success',
                body: 'Pipeline ran successfully.',
                to: 'zeyardh123suffian@gmail.com'
            )
        }
        failure {
            emailext(
                subject: 'Pipeline Failure',
                body: 'Pipeline failed.',
                to: 'zeyardh123suffian@gmail.com'
            )
        }
    }
}
