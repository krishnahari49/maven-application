node{

def MavenVersion = tool name: "maven3.9.12"
properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '2', numToKeepStr: '3'))])

stage('GitCode'){
git branch: 'development', url: 'https://github.com/krishnahari49/maven-application.git'
}

stage('Build'){
sh "${MavenVersion}/bin/mvn clean package"
}

stage('SonarWay'){
sh "${MavenVersion}/bin/mvn sonar:sonar"
}

stage('NexusUpload'){
sh "${MavenVersion}/bin/mvn deploy"
}

stage('UploadTomcat'){
sh "scp target/maven-application.war /opt/apache-tomcat-10.1.49/webapps/maven-application.war"
}

}
