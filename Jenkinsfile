pipeline {
    agent any

    triggers {
        githubPush()   
    }

    stages {

        stage('Clone') { steps { git url: 'https://github.com/hind0074/cargo-tracker-UM6P1.git', branch: 'main' } }

        stage('Build & Test with Coverage') {
            steps {
                bat 'mvn clean verify'
            }
        }

        
    }
//
    post {
        success {
            echo 'Build et analyse terminés avec succès !'
        }
        failure {
            echo 'Échec du build ou des tests.'
        }
    }
}
