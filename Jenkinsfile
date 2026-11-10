
pipeline {
    agent any

    environment {
        JAVA_HOME = 'C:\\Program Files\\Amazon Corretto\\jdk21.0.9_10'
        PATH+JAVA = 'C:\\Program Files\\Amazon Corretto\\jdk21.0.9_10\\bin'
        PATH+MAVEN = 'C:\\Users\\SHRUTHI\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
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

