pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					sh '''
						env.Variable='True'
					'''
				}
			}


			stage('Second') {
				when {
				    expression { env.Variable=='True' }
				}
				steps {
					sh '''
						echo "Updating Second Stage"
					'''
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
