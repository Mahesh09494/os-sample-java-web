pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               sh 'url:https://github.com/Mahesh09494/os-sample-java-web.git, branch:/master credentialsid:admin'

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
