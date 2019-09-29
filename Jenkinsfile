pipeline
{
	agent any
		{
			stage "scm checkout" {
	    git 'https://github.com/surabhi2893/maven-project.git'
				
			}
	
	
	    stage "code test"
	    withMaven(maven: 'LocalMaven'){
	    sh 'mvn test'
	    }
	
	}
	
}
