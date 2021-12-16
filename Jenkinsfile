pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') {
				steps {
					sh '''
						echo "Step Three ${env.VariableT}"
					'''
					env.VariableT = true
				}
			}
			
			when {
				
			 expression { $VariableT == true }
				anyOf {
				stage('Second') {
					steps {
						sh '''
							echo "Updating Second Stage"
						'''
					}
				} 
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
