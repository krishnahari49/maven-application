node{

def mavenHome = tool name: "maven3.9.9"

stage('GitCheckOut'){
git branch: 'development', credentialsId: 'af9ead25-3935-4be9-9cca-12f86fc6501f', url: 'https://github.com/krishnahari49/maven-application.git'
}
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
}
