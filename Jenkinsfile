pipeline {
    agent any
    tools {
        nodejs 'TINode-devops'
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
            steps{
                echo 'NodeJS configuration gebruiken: TINode-devops'
                sh 'node --version'
                sh 'npm --version'
            }
        }
        }
    }
}