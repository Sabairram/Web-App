pipeline{
agent any
tools{
maven 'maven'
} stages {
stage('Build Maven'){
steps{
script{
checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url:
'https://github.com/Sabairram/Web-App.git']])
bat 'mvn clean install'
} }
stage('Build docker image'){
steps{
script{
bat 'docker build -t sabairram/webapp .'
}}} }}}
