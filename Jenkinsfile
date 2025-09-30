pipeline {
    agent any
    
    tools {
        maven 'maven-3'
        jdk 'jdk17'
    }
    
    stages {
        stage('Git checkout') {
            steps {
                git branch: 'DR', url: 'https://github.com/ShavB/boardgame-java.git'
            }
        }
        stage('Compile') {
            steps {
               sh '''mvn compile'''
            }
        }
        stage('Test') {
            steps {
                sh '''mvn test'''
            }
        }
        stage('Create packages') {
            steps {
                sh '''mvn package'''
            }
        }
        stage('Job finished') {
            steps {
                echo 'hehehhe gooood job'
            }
        }
    }
}
