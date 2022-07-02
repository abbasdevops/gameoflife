pipeline {
	agent any
	stages {
        	stage('Initialize'){
            		steps{
                		set "PATH = 'D:\\DevOps course tech\\apache-maven-3.8.6\\bin' "
				set "JAVA_HOME = 'C:\\Program Files\\Java\\jre-9.0.4' "
                
            }
        }
                
	
		stage('build') {
			steps {
				bat 'mvn clean package'
			}
		}
    }
}
