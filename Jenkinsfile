pipeline {
    agent any

    stages {
        stage ('Clone') {
            steps {
                git url: 'https://github.com/akshatha1992/XQT-Project.git'
            }
        }
        stage ('Initital Setup') {
            steps {
               bat label: '', script: 'cd C:\\Docker\\MSGFW2.0'
            }
        }
        stage ('Docker Build') {
            steps {
               bat label: '', script: 'docker build -t msgfw2.0 .'
            }
        }
        stage ('Execution') {
            steps {
                 bat label: '', script: 'docker build --pull --target testrunner -t msgfw2.0:test .'
            }
        }
        stage ('Report') {
            steps {
               bat label: '', script: 'docker run --rm -v "C:\\Docker\\TestResults":C:\\app\\msg.Testframework_cs\\TestResults msgfw2.0:test'
            }
        }

        
    }
}
