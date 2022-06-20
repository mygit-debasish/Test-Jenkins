CODE_CHANGE = true
pipeline {
	agent any 

	 stages {
	 	
		 stage("build"){
			 
	 		steps {
	 			echo 'Building the applications ... adding to Github from new branch newBranch , again change'
	 		}
	 	}
	 	stage("Test") {
	 		when {
	 			expression {
	 				BRANCH_NAME == 'newBranch' && CODE_CHANGE == true
					//BRANCH_NAME == 'newBranch'
	 			}
	 		}
	 		steps {
	 			echo 'Testing the applications..'
				//echo 'Chnage detected !!'
	 		}
	 	}

	 	stage("Deploy") {
	 		steps {
	 			echo 'Deploying applications..'
	 		}
	 	}

	 }

	 post {
	 	success {
			echo 'Post applications'
	 		echo 'Success !!'
		}
		
	}
}