pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
    	pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''#!/bin/bash
				python3 -m venv .venv
				source .venv/bin/activate
                cd myapp
                pip3 install -r requirements.txt --use-pep517
                echo "doing build stuffasdadasd.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''#!/bin/bash
                source .venv/bin/activate
                cd myapp
                python3 hello.py
                python3 hello.py --name=mariano
                echo "doing test stuffjhjjujj.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
