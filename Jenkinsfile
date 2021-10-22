pipeline {
    agent any
    stages {
        stage('checkout')
        {
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url:'https://github.com/Harish1290/demolocustproject.git']]])
            }
        }
        stage('build')
        {
            steps{
                git 'https://github.com/Harish1290/demolocustproject.git'
               bat 'locust --config=locust.yml --html htmlreport.html'
            }
        }
    }
}
