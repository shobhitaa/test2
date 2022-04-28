pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '0cf140bd-aeed-4bca-ac16-54ac29901246', url: 'https://github.com/shobhitaa/test2.git']]])
            }
        }
        stage('Build') {
            steps{
                git branch: 'main', credentialsId: '0cf140bd-aeed-4bca-ac16-54ac29901246', url: 'https://github.com/shobhitaa/test2.git'
                bat 'python testfile.py'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing successful'
            }
        }
    }
}
