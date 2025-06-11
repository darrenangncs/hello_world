pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://github.com/dennisang-NCS/HelloWorld.git'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java program and package it
                bat 'mvn package'
            }
        }
        stage('Run') {
            steps {
                // Run the Java program
                bat 'java -cp target/classes com.example.App'
            }
        }
    }
}
