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
				
					ANYPOINT_CREDENTIALS = credentials('8e5b4d44-467c-4840-af90-ce4515b4bb0a')
				
				}
			
				steps {
				
					echo 'Deploying mule project due to the latest code commit…'
				
					echo 'Deploying to the configured environment….'
				
					bat 'mvn -e -X clean deploy -DmuleDeploy -Dmule.app.name=arithmetic-api -Dusername=%Alexo12% -Dpassword=%Alex!123!% -DworkerType=Micro -Denv=dev'
				
				}
		
		}
	}
} 