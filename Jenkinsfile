pipeline {
    agent any

    tools {
        maven 'Maven 3.9.4' // Adjust the Maven version as needed
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/darrenangncs/hello_world.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            junit '**/target/surefire-reports/*.xml'
            archiveArtifacts artifacts: '**/target/*.jar', allowEmptyArchive: true
        }
    }
}
