pipeline {
    agent any
    tools {
        maven 'mvn'
        jdk 'jdk8'
    }
    stages {

         stage ('Test') {
                    steps {
                        echo 'Running tests'
                        sh 'mvn clean test'
                    }
                }

        stage ('Build') {
            steps {
                echo 'Build'
                sh 'mvn clean package'
            }
        }
    }
}