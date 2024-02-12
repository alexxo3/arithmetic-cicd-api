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
				
					ANYPOINT_CREDENTIALS = credentials('95732392-d8b3-413b-9059-98449543a3c0')
				
				}
			
				steps {
				
					echo 'Deploying mule project due to the latest code commit…'
				
					echo 'Deploying to the configured environment….'
				
					bat 'mvn -e -X clean deploy -DmuleDeploy -Dmule.app.name=arithmetic-api -Dusername=%Alexo12% -Dpassword=%Alex!123!% -DworkerType=Micro -Denv=dev'
				
				}
		
		}
	}
} 