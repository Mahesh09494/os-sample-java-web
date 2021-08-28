pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               bat 'url:https://github.com/Mahesh09494/os-sample-java-web.git, branch:/main, credentialsid:Mahesh09494'

  }
        }
        stage('build') {
            steps {
                bat 'mvn clean install'
            }
        }
         stage('Deploy') {
            steps {
		bat 'cp os-sample-java-web/targrt/*.war c:/programfiles/tomcat/webapp/'
        }
    }
    }
}
