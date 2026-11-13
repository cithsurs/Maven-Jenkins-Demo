
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Maven Build'
                bat 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                bat 'java -cp target/classes Hello'
            }
        }
    }

    post {
        success {
            echo 'Maven Jenkins Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline execution failed!'
        }
    }
}
