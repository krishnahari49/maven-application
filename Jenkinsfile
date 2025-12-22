node{

def MavenVersion = tool name: "maven3.9.12"

stage('GitCode'){
git branch: 'development', url: 'https://github.com/krishnahari49/maven-application.git'
}

stage('Build'){
sh "${MavenVersion}/bin/mvn clean package"
}

stage('SonarWay'){
sh "${MavenVersion}/bin/mvn sonar:sonar"
}

}
