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

