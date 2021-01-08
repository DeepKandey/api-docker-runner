pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
			    //sh
				bat "docker pull deepkandey/apitesting_practice"
			}
		}
		stage("Run Test"){
			steps{
			    //sh
				bat "docker-compose up"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
		    bat "rmdir /S /Q output"
		}
	}
}
