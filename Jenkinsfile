pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven"
        jdk "Java"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                //git 'https://github.com/abbasdevops/gameoflife.git'

                // Run Maven on a Unix agent.
                //sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                bat "mvn -Dmaven.test.failure.ignore=true clean package"
                //bat "mvn clean package"
            }
        }
       stage('TomcatDeploy') {
            steps { 
                deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://localhost:8081/')], contextPath: 'gameoflife1', war: '**/*.war'
            }
       } 
       stage('Publish-To-Nexus') {
            steps { 
                //nexusArtifactUploader artifacts: [[artifactId: 'gameoflife', classifier: '', file: 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\Declarative-Pipeline-Java\\gameoflife-web\\target\\gameoflife.war', type: 'war']], credentialsId: 'nexus-2password', groupId: 'com.wakaleo.gameoflife', nexusUrl: 'localhost:8083/nexus/content/ ', nexusVersion: 'nexus3', protocol: 'http', repository: 'releases', version: '1.1'
                nexusPublisher nexusInstanceId: 'Releases', nexusRepositoryId: 'releases', packages: [[$class: 'MavenPackage', mavenAssetList: [[classifier: '', extension: '', filePath: 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\Declarative-Pipeline-Java\\gameoflife-web\\target\\gameoflife.war']], mavenCoordinate: [artifactId: 'gameoflife', groupId: 'com.wakaleo.gameoflife', packaging: 'war', version: '1.5']]]
            }
         } 
    }
}
