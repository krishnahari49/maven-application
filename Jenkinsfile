pipeline{
agent any
stages{
stage('GithubCheckout'){
steps{
git branch: 'development', credentialsId: 'af9ead25-3935-4be9-9cca-12f86fc6501f', url: 'https://github.com/krishnahari49/maven-application.git'
}
}
}//stages closing
}//pipeline closing
