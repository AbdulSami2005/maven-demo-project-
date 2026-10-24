pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                // If maven is globally installed on your system, 'mvn' works directly
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
