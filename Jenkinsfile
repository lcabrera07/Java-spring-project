pipeline {
	agent any
	tools {
    	maven 'local-mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'main',  url: 'https://github.com/lcabrera07/Java-spring-project'         	 
        	}    
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	    }
        }
    	stage("Package") {          	 
        	steps {  	 
            	sh "mvn package"          	 
       	    }
        }
    }
}
