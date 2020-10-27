pipeline {
    agent any
    stages {
        stage ('package stage') {
            steps {
			node ('buildagent') {
               sh 'mvn clean package'
			   sh label: '', script: 'sudo docker image build -t delixus .'
			   }               
            }
        }
    }
}
