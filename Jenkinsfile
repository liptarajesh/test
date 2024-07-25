pipeline {
    agent any  // Executes the pipeline on any available agent (node)

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo.git'  // Replace with your Git repository URL
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Example Maven build command
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'  // Example Maven test command
            }
        }

        stage('Deploy') {
            steps {
                sh 'bash deploy.sh'  // Example deployment script
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! This is where you can send notifications.'
        }
        failure {
            echo 'Pipeline failed! This is where you can handle failure cases.'
        }
    }
}
