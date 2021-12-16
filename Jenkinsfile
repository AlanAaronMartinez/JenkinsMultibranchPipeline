pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') { 
							
				steps {
					script{
					env.VariableT = true
					sh '''
					echo "Step Three ${VariableT}"
					'''
					}
					 
					
					
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
