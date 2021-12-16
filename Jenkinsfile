pipeline {
	agent any
	  environment { 
          VariableT = false
    	  }
		stages {
			stage('First') {
				steps {
					sh '''
						echo "Step Three ${VariableT}"
					'''
					VariableT = true
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
