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
                sh '''
                cd myapp
                pip3 install -r requirements.txt
                echo "doing build stuffasdadasd.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
				cd myapp
                python3 hello.py
                python3 hello.py --name=Mariano
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
