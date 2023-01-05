pipeline{
	agent any
	triggers {
  		pollSCM '* * * * *'
	}

	stages{
		stage ('git'){

			steps{
			checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/spring-projects/spring-petclinic.git']])
			}

		} //stage one completed
		
		stage('Build'){

			steps{
			sh 'mvn package'
			
			}
		}

	}

}
