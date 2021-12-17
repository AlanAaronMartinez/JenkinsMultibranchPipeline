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
				
		
				stage('Second') {
					
				when {
				
				 expression { VariableT ==~ true }
					steps {
						sh '''
							echo "Updating Second Stage ${VariableT}"
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
