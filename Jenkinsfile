pipeline {
     agent {labels 'Jenkins-Agent'}
     tools{
	jdk 'Java17'
	maven 'Maven3'
     }
     stages{
	     stage("Clean Workspace"){
		     steps{
			     cleanWs()
		     }
	     }
	     stage("Checkout from SCM"){
		     steps{
			     git branch: 'main', credentialsId: 'Megboko', url: 'https://github.com/Mitchxxx/register-app'
		     }
	     }

	     stage("Build Application"){
		     steps{
			     sh "mvn clean package"
		     }
	     }
	     stage("Test Application"){
		     steps{
			     sh "mvn test"
		     }	     
	     }
	     
	  }
}
