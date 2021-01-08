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
				bat "docker run deepkandey/apitesting_practice"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'test-output/**'
		    bat "rmdir /S /Q test-output"
		}
	}
}
