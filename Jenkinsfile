pipeline {
	agent any
	stages {
        	stage('Initialize'){
            		steps{
                		echo "PATH = 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin' "
				echo "PATH = %JAVA_HOME% "
				echo "JAVA_HOME: C:\\Program Files\\Java\\jdk-9.0.4"
                
            }
        }
                
	
		stage('build') {
			steps {

				bat "mvn clearn package"
			}
		}
    }
}
