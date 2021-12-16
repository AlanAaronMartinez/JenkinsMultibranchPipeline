pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') {
				environment { 
        				  env.VariableT = true
    	 				 }
				steps {
					 
					sh '''
						echo "Step Three ${VariableT}"
					'''
					
				}
			}
			
			
	
			stage('Third') {
				steps {
					sh '''
						echo "Step Three ${VariableT}"
					'''
				}
			}
		}
}
