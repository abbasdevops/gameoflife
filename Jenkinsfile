pipeline {
	agent any
	stages {
        	stage('Initialize'){
            		steps{
                		echo "PATH = 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin' "
				echo "PATH = JAVA_HOME: %JAVA_HOME%"
				
                	
            }
        }
                
	
		stage('build') {
			steps {

				bat " 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin\\mvn.cmd' clean package"
			}
		}
    }
}
