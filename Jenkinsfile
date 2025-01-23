pipeline {
    agent any
    tools {
        nodejs 'TINnode-devops'
    }
    stages {
        stage('opdracht 5') {
            steps {
                echo "good luck..."
            }
        }
        stage('fetching source'){
            steps{
                git branch: 'main',
                    url: 'git@github.com:mohaimenpxl/calculator-app-finished.git',
                    credentialsId: 'github'
            }
        stage('Setup NodeJS'){
            echo 'NodeJS configuration gebruiken: TINnode-devops'
                sh 'node --version'
                sh 'npm --version'
        }
        }
    }
}