pipeline {
	agent any
	tools {
    	maven 'my_mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'master',  url: 'https://github.com/lcabrera07/Java-spring-project'         	 
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
