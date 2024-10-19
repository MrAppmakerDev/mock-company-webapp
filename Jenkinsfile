pipeline {
    agent any

    stages {
        stage('Assemble') {
            steps {
                echo 'Assembling the project...'
                sh './gradlew clean assemble'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Build and tests succeeded!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}
