pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME'  // Ensure this matches your Jenkins Maven tool configuration
    }
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/HARIVIGNESHRAO/SELABJenkins.git', branch: 'main'
            }
        }
        stage('Clean') {
            steps {
                bat 'mvn clean'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'mvn install'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
    }
}
