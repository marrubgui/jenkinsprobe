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
                bash
                python3 -m venv .venv
                source
		ls
                echo "doing build stuffasdadasd.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
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
