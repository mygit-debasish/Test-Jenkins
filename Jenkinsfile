CODE_CHANGE = true
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
	 				//BRANCH_NAME == 'main' && CODE_CHANGE== true
					BRANCH_NAME == 'main'
	 			}
	 		}
	 		steps {
	 			echo 'Testing the applications..'
				echo 'Chnage detected !!'
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
