pipeline {
    agent any

    parameters {
        string(name: 'BRANCH', defaultValue: 'master', description: 'Git Branch')
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: "${params.BRANCH}",
                url: 'https://github.com/shaikhshahbazz/spring3-mvc-maven-xml-hello-world-1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
