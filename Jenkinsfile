
pipeline {
	

withMaven(globalMavenSettingsConfig: 'null', jdk: 'Java', maven: 'Maven', mavenSettingsConfig: 'null') {
    // some block
}
	
	agent any
	
	stages {
		stage('build') {
			steps {
				bat 'mvn clean package'
			}
		}
    }
}
