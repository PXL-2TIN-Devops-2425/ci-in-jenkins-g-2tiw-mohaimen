pipeline {
    agent any
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
        }
    }
}