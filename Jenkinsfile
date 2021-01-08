pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
			    //sh
				bat "docker pull deepkandey/apitest"
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
			archiveArtifacts artifacts: 'output/**'
		    bat "rmdir /S /Q output"
		}
	}
}
