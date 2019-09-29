pipeline 
{
	agent any
	
	stages
	{
		stage ('scm checkout') {
	    	git 'https://github.com/surabhi2893/maven-project.git'
		}
	}
	{
	
		stage ('code test') {
		steps {
	    		withMaven(maven: 'LocalMaven')
				{
				sh 'mvn test'
	    			}
			}
		}
	}
}

stage ('deploy to tomcat'){

steps {
  sshagent (['35.180.189.169']) {
    sh 'scp -o StrictHostKeyChecking=no **/*war ec2-user@35.180.189.169:/var/lib/tomcat/webapps
	}
  }
}

