pipeline{
	agent any
	tools{
		maven 'apache-maven'
		jdk 'jdk1.8.0_171'
	}
	stages{
		stage('Build'){	
			steps{
			bat 'mvn install'
			}
			post {
				always{
					junit 'target/surefire-reports/*/.xml'
				}
			}
		}

	}
}
