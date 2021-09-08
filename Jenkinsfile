pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mahesh09494/os-sample-java-web.git']]])

  }
        }
        stage('build') {
            steps {
                sh 'mvn clean install'
            }
        }
         stage('Deploy') {
            steps {
		sh 'cp os-sample-java-web/target/*.war c:/programfiles/tomcat/webapp/'
        }
    }
    }
}
