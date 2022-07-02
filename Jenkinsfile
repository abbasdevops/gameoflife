withMaven(globalMavenSettingsConfig: 'null', jdk: 'Java', maven: 'Maven', mavenSettingsConfig: 'null', mavenSettingsFilePath: '"D:\\DevOps course tech\\apache-maven-3.8.6\\conf\\settings.xml"', tempBinDir: 'C:\\Program Files\\Java\\jdk-9.0.4') {
    // some block
}
pipeline {
	agent any
	
	stages {
		stage('build') {
			steps {
				bat 'mvn clean package'
			}
		}
    }
}
