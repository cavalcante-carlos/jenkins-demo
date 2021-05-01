pipeline {
    agent any

    tools {
        gradle 'Gradle-7.0'
    }

    stages {
        stage("run frontend"){
            steps {
                echo 'executing yarn...'
                nodejs ('NodeJS-16.0.0'){
                    sh 'yarn install'
                }   
            }
        }
        stage ("run backend"){
            steps {
                echo 'executing gradle...'
                sh './gradlew -v'
            }
        }
    }
}