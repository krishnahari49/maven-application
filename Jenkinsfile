node{

def mavenHome = tool name: 'maven3.9.9'

stage('Gitcheck'){
git branch: 'questions', credentialsId: 'af9ead25-3935-4be9-9cca-12f86fc6501f', url: 'https://github.com/krishnahari49/maven-application.git'
}
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
stage('sonarBuild'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('UploadNexus'){
sh "${mavenHome}/bin/mvn deploy"
}
stage('Copyfiles'){
sh "scp target/maven-application.war /tmp/"
}
}//node closing
