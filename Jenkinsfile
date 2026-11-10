

pipeline {
    agent any

    environment {
        JAVA_HOME = 'C:\\Program Files\\Amazon Corretto\\jdk21.0.9_10'
        MAVEN_HOME = 'C:\\Users\\SHRUTHI\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'set "PATH=%JAVA_HOME%\\bin;%MAVEN_HOME%\\bin;%PATH%" && mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'set "PATH=%JAVA_HOME%\\bin;%MAVEN_HOME%\\bin;%PATH%" && mvn test'
            }
        }

        stage('Package') {
            steps {
                bat 'set "PATH=%JAVA_HOME%\\bin;%MAVEN_HOME%\\bin;%PATH%" && mvn package'
            }
        }
    }
}
