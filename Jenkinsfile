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
                echo 'CICD Process'
            }
        }
	stage ('Execution Selenium Script from Local Machine') {
	    steps 
	    {
	   bat label: '', script: '''cd "C:\\CICD_Jenkins"
	   "C:\\Program Files (x86)\\ojdkbuild\\java-1.8.0-openjdk-1.8.0.222-2\\jre\\bin\\java" -jar SeleniumWebPage.jar'''
	    }
        }
        stage ('Report') {
            steps {
                echo "Report Details"
            }
        }

        
    }
}
