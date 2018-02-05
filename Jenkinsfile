pipeline {
    // agent { docker 'maven:3.3.9' }

		agent any
    stages {
        stage('deploy - staging') {
            steps {
								sh './deploy.sh staging'
								sh './run-smoke-tests.sh'
            }
        }
        stage('sanity check') {
            steps {
							 input 'Does the staging environment looks OK?'	
            }
        }
        stage('deploy - production') {
            steps {
								sh './deploy.sh production'
            }
        }
		}
}
