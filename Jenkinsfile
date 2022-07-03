pipeline {
	agent any
	stages {
        	stage('Initialize'){
            		steps{
                		echo "PATH = 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin' "
				SET "JAVA_HOME: C:\\Program Files\\Java\\jre-9.0.4"
				
                	
            }
        }
                
	
		stage('build') {
			steps {

				bat " 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin\\mvn.cmd' clean package"
			}
		}
    }
}
