pipeline {
    agent any
    tools {
        gradle 'Gradle'   // <- match the name you configured
    }
    stages {
        stage("run frontend") {
            steps {
                echo 'executing yarn...'
                nodejs('Node-23.11') {
                    bat 'yarn install'
                }
            }
        }
        stage("run backend") {
            steps {
                echo 'executing gradle...'
                bat 'gradle -v'   // Now using the installed Gradle
            }
        }
    }
}
