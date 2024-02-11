pipeline{

	agent any
	
	stages {
	
			stage('Build Application') {
			
					steps {
					
						bat 'mvn clean install'
					
					}
				}
				
			stage('Deploy CloudHubs') {
			
				environment {
				
					ANYPOINT_CREDENTIALS = credentials(' ')
				
				}
			
				steps {
				
					echo 'Deploying mule project due to the latest code commit…'
				
					echo 'Deploying to the configured environment….'
				
					bat 'mvn clean deploy -DmuleDeploy  -Dusername=%Alexo12% -Dpassword=%Alex@ms2024% -DworkerType=Micro -Denv=dev'
				
				}
		
		}
	}
} 