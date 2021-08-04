ipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mahesh09494/os-sample-java-web.git']]])
            }
        }
        stage('build') {
            steps {
                bat 'mvn clean install'
            }
        }
         stage('Deploy') {
            steps {
deploy adapters: [tomcat9(credentialsId: 'Tomcat', path: '', url: 'http://localhost:8088/')], contextPath: 'Root', war: '**/*.war'
        }
    }
    }
}
