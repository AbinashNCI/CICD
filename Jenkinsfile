pipeline {
    agent any
//
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/AbinashNCI/CICD.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package' // Change for Node.js, Python, etc.
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test' // Replace with your testing framework
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add Docker, Kubernetes, or AWS commands here
            }
        }
    }
}
