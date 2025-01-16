pipeline{
agent any
tools{
maven 'maven3.9.9'
}
stages{

stage('GithubCheckout'){
steps{
git branch: 'development', credentialsId: 'af9ead25-3935-4be9-9cca-12f86fc6501f', url: 'https://github.com/krishnahari49/maven-application.git'
}
}
stage('Build'){
steps{
sh "mvn clean package"
}
}
}//stages closing
}//pipeline closing
