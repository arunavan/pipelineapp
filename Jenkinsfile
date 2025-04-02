pipeline {
    agent any
    tools{
        maven : 'maven1'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean'
                }
            }
        }
    }
}
