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
					environment name: 'VariableT', value: true
				     }
					steps {
						sh '''
							echo "Updating Second Stage ${VariableT}"
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
