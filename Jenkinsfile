pipeline {
	agent any
	  
		stages {
			stage('First') { 
							
				steps {
					script{
					env.VariableT = true
					sh '''
					echo "Step ONE ${VariableT}"
					'''
					}
					 
					
					
				}
			}
				
		when {
				
			 expression { VariableT == true }
				anyOf {
				stage('Second') {
					steps {
						sh '''
							echo "Updating Second Stage ${VariableT}"
						'''
					}
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
