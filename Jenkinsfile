pipeline {
	agent any
	  
		stages {
			stage('First') { 		
				steps {
					script{
					env.VariableT = false
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
				when {
					environment name: 'VariableT', value: 'false'
				     }
				steps {
					sh '''
						echo "Step Three ${VariableT}"
					'''
				}
			}
		}
}
