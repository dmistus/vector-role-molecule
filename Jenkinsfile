pipeline {
    agent any

    stages {
        stage('GIT checkout') {
            steps {
                echo 'Get from GIT repository'
                git credentialsId: '805a71d5-bb9e-4aca-8e89-e9ae0233200d',
                url: 'git@github.com:dmistus/vector-role-molecule.git',
                branch: 'main'
            }



    }
}
