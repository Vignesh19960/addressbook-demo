pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/Vignesh19960/addressbook-demo.git'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git GIT_REPO
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'  // Builds the JAR/WAR file
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
