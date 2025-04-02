pipeline {
    agent any
    tools {
        maven 'maven1'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'echo "Checking Maven Installation..."'
                    sh 'mvn --version'  // Verify Maven is detected
                    sh 'mvn clean'
                }
            }
        }
    }
}
