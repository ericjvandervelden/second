pipeline {
    // agent { docker 'maven:3.3.9' }
		agent any
    stages {
        stage('build') {
            steps {
                sh 'mvn --version;echo $$'
								sh ' echo "Hello World";echo $$'
								sh '''
										echo "Multiline shell steps work too"
										ls -alh
										echo $$
										echo $$
								'''
            }
        }
    }
}
