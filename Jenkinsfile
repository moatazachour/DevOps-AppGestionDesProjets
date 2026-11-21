pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout Git') {
            steps {
                checkout scm
            }
        }

        stage('Maven Build') {
            steps {
                dir('backend') {
                    sh 'mvn clean compile'
                }
            }
        }
    }
}
