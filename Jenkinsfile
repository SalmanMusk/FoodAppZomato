pipeline {
    agent any

    environment {
        // Define any environment variables here
        APP_NAME = 'FoodAppZomato'
    }

    tools {
        // Configure necessary tools
        jdk 'JDK_11' // Specify JDK version
        maven 'Maven_3.6.3' // Specify Maven version
        docker 'Docker_19.03.1' // Specify Docker version if needed
    }

    stages {
        stage('Build') {
            steps {
                script {
                    // Your build commands here, e.g., using Maven
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Your test commands here, e.g., unit tests
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Your deploy commands here
                    echo 'Deploying application...'
                    // For example: sh './deploy.sh'
                }
            }
        }
    }

    post {
        always {
            // Cleanup activities or notifications
            echo 'Cleaning up...'
        }
    }
}