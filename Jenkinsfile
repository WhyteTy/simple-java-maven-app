pipeline {
    agent any

    environment {
        MAVEN_HOME = tool name: 'Maven 3.9.9', type: 'maven'
    }

    stages {
        stage('Pull Latest Changes') {
            steps {
                bat 'git pull origin master'
            }
        }

        stage('Merge Feature Branch') {
            steps {
                bat 'git merge origin/features'
            }
        }

        stage('Push Merged Changes') {
            steps {
                bat 'git push origin master'
            }
        }
    }
}