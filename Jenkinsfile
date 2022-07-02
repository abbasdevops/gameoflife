pipeline {
	agent any
	tools {
        maven "MAVEN"
        jdk "JDK"
    }
	stages {
        stage('Initialize'){
            steps{
                echo "PATH = 'D:\DevOps course tech\apache-maven-3.8.6\bin' "
                
            }
        }
                
	
		stage('build') {
			steps {
				bat 'mvn clean package'
			}
		}
    }
}
