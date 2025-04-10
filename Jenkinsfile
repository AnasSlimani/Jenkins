pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
                echo 'executing yarn...'
                nodejs('Node-23.11'){
                  bat 'yarn install'
                }
            }
        }
        stage("run backend") {
            steps {
                echo 'executing gradle...'
                withGradle(){
                  bat './gradlew -v'
                }
            }
        }
    }
}
