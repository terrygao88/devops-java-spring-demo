pipeline {
	agent any
	tools {
    	maven 'local-mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'main',  url: 'https://github.com/terrygao88/devops-java-spring-demo'          	 
           	 
        	}    
    	}
    	stage('Build') {
        	steps {
        	sh "mvn build"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	    }
        }
        stage ('Package') {
                steps {
                sh "mvn package"
            }
        }		
    }
}
