pipeline {
    //agent { docker 'maven:3.3.9' }
		agent any
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
