pipeline {
    agent {
        label 'ansible'
    }
    stages {
        stage('Git') {
            steps{
                git branch: 'main', credentialsId: '805a71d5-bb9e-4aca-8e89-e9ae0233200d', url: 'https://github.com/dmistus/vector-role-molecule.git'
            }
        }
        stage('Molecule install') {
            steps{
                sh 'pip3 install molecule==3.4.0'
                sh 'pip3 install ansible-lint==5.1.3'
                sh 'pip3 install molecule_docker'
            }
        }
        stage('Molecule test'){
            steps{
                dir('roles/vector-role/') {
                    sh 'ls -l'
                    sh 'molecule test'
                    cleanWs()
                }
            }
        }
    }
}
