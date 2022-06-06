CODE_CHANGE = getGitChanges()
pipeline {
	agent any 

	 stages {
	 	
		 stage("build"){
			 
	 		steps {
	 			echo 'Building the applications ...'
	 		}
	 	}
	 	stage("Test") {
	 		when {
	 			expression {
	 				BRANCH_NAME == 'dev' && CODE_CHANGE== true
	 			}
	 		}
	 		steps {
	 			echo 'Testing the applications..'
	 		}
	 	}

	 	stage("Deploy") {
	 		steps {
	 			echo 'Deploying applications..'
	 		}
	 	}

	 }

	 post {
	 	//
	 }
	 success {
	 	//
	 }
	 failure {
	 	//
	 }

		
	}
