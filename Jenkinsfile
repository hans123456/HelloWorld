pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                script {
                    if (isUnix()){
                      sh './gradlew compileJava --info'
                    } else {
                      bat 'gradlew.bat compileJava --info'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                script {
                    if (isUnix()){
                      sh './gradlew test --info'
                    } else {
                      bat 'gradlew.bat test --info'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}