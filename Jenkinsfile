pipeline {
    agent { docker 'maven:3.3.9' }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
								sh ' echo "Hello World"'
								sh '''
										echo "Multiline shell steps work too"
										ls -alh
								'''
            }
        }
    }
}
