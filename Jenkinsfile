pipeline {
	agent any
	  
		stages {
			stage('First') { 		
				steps {
					script{
					env.VariableT = true
					sh '''
					echo "First Stage. The variable is: ${VariableT}"
					'''
					}
				}
			}
				stage('Second') {
				when {
					environment name: 'VariableT', value: 'true'
				     }
					steps {
						sh '''
							echo "Second Stage. The variable is: ${VariableT}"
						'''
					}
				}
			
			stage('Third') {
				when {
					environment name: 'VariableT', value: 'false'
				     }
				steps {
					sh '''
						echo "Third Stage. The variable is: ${VariableT}"
					'''
				}
			}
		}
}
