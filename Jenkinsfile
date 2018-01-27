pipeline {
    // agent { docker 'maven:3.3.9' }
		agent any
    stages {
        stage('deploy') {
            steps {
							retry(3){
								sh './flakey-deploy.sh'
							}
							timeout(time:3,unit:'SECONDS'){
								sh './health-check.sh'
							}
            }
        }
    }
}
