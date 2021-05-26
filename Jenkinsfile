pipeline {
    agent any
    stages {
        stage('Clone Repositry & clean') {
            steps {
                sh 'git clone https://github.com/sunilmaury/jenkinsfile.git'
                sh 'mvn clean -f jenkinsfile'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -f jenkinsfile'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package -f jenkinsfile'
            }
        }
    }
}
