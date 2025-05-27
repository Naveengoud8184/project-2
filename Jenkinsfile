pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    environment {
        PATH = "/opt/apache-maven-3.9.9/bin:$PATH"
    }

    stages {
        stage('clone-code') {
            steps {
                git branch: 'main', url: 'https://github.com/Naveengoud8184/project-2.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
