pipeline {
    agent any
    tools {
        maven '3.5.2'
        jdk '1.8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

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