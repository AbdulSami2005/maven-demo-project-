pipeline {
    agent any

    tools {
        // This matches the Name 'maven' field configured in your Jenkins UI screenshot
        maven 'maven'
    }

    stages {
        stage('Compile Stage') {
            steps {
                // Jenkins will now automatically locate 'mvn' via your MAVEN_HOME configuration
                sh 'mvn clean compile'
            }
        }

        stage('Testing Stage') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deployment Stage') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }
}
