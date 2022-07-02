
pipeline {
	agent any
	tools {
        maven "MAVEN"
        jdk "JDK"
    }
	stages {
		stage('build') {
			steps {
				bat 'mvn clean package'
			}
		}
    }
}
