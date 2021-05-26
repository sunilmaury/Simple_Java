pipeline {
    agent any
    stages {
        stage('Clone Repositry & clean') {
            steps {
                sh 'git clone https://github.com/sunilmaury/Simple_Java.git'
                sh 'mvn clean -f Simple_Java'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test -f Simple_Java'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package -f Simple_Java'
            }
        }
    }
}
