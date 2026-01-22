pipeline {
    agent any

    triggers {
        githubPush()   
    }
//test 
    stages {

        stage('Clone') { steps { git url: 'https://github.com/hind0074/cargo-tracker-UM6P1.git', branch: 'main' } }

       

        
    }

    post {
        success {
            echo 'Build et analyse terminés avec succès !'
        }
        failure {
            echo 'Échec du build ou des tests.'
        }
    }
}
