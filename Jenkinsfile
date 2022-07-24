pipeline {
    agent any
    tools {
        maven 'MVN_version'
    }
    stages {
        stage('SourceCode') {
            steps {
                git branch: 'main', url: 'https://github.com/arvindmahat/spring-petclinic.git'
            }
        }
        stage('Build image') {
            steps {
                sh 'docker image build -t myimage:1.0 .'
            }
        }
    }
}
