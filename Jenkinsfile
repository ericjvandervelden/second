pipeline {
    // agent { docker 'maven:3.3.9' }
		agent any
    stages {
        stage('deploy') {
            steps {
							retry(3){
								sh 'echo "Fail";exit 1'
							}
            }
        }
		}
		post{
			always{
				echo 'This will always run'
			}
			success{
				echo 'This will only if successful'
			}
			failure{
				//echo 'This will run only if failed'
				mail to:'ericjvandervelden@gmail.com',
				subject:"Failed pipeline:${currentBuild.fullDisplayName}",
				body:"Something is wrong with ${env.BUILD_URL}"
			}
			unstable{
				echo 'This will run only if the run was marked unstable'
			}
			changed{
				echo 'This will run only if the status of the pipeline has changed'
				echo 'for example if the pipeline was previously failing but now is successful'
			}
    }
}
