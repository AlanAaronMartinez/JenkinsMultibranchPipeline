pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') {
				steps {
					VariableT= true
				}
			}
			
			when {
				
			 expression { env.VariableT == true }
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
