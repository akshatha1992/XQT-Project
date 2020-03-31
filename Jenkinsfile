pipeline {
    agent any

    stages {
        stage ('Clone') {
            steps {
                git url: 'https://github.com/akshatha1992/Sample-Test-Repository.git'
            }
        }
        stage ('Initital Setup') {
            steps {
                input('In pipeline, We take decision. Can we proceed?')
            }
        }
        stage ('Execution') {
            steps {
                echo "PATH = ${PATH}"
                echo "Java_HOME = ${JAVA_HOME}"
            }
        }
        stage ('Report') {
            steps {
                echo "Report Details"
            }
        }

        
    }
}
