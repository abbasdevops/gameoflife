pipeline {
	agent any
	stages {
        	stage('Initialize'){
            		steps{
                		echo "PATH = 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin' "
				echo "JAVA_HOME = C:\\Program Files\\Java\\jre-9.0.4 "
                
            }
        }
                
	
		stage('build') {
			steps {
				echo "JAVA_HOME = C:\\Program Files\\Java\\jre-9.0.4 "
				bat 'mvn clean package'
			}
		}
    }
}
