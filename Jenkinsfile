pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') {
				steps {
					 environment { 
        				  VariableT = true
    	 				 }
					sh '''
						echo "Step Three ${VariableT}"
					'''
					
				}
			}
			
			

			stage('Third') {
				steps {
					sh '''
						echo "Step Three"
					'''
				}
			}
		}
}
