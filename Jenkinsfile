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
        stage ('Get Java Home Path') {
            steps {
                echo "PATH = ${PATH}"
                echo "Java_HOME = ${JAVA_HOME}"
            }
        }
	 
	stage ('Execute Selenium Script from Git Repo ') {
            steps {
                bat label: '', script: 'executeTest.bat'
            }
        }
	
	stage ('Execution Selenium Script from Local Machine') {
	    steps 
	    {
	   bat label: '', script: '''cd C:\\Jenkins\\SampleDemo
	  "C:\\Program Files (x86)\\ojdkbuild\\java-1.8.0-openjdk-1.8.0.222-2\\jre\\bin\\java" -jar "PipelineSeleniumDemo.jar"'''
	    }
        }
        stage ('Report') {
            steps {
                echo "Report Details"
            }
        }

        
    }
}
