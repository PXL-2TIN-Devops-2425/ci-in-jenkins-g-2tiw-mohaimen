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
        }
        stage('Setup NodeJS'){
            steps{
                echo 'NodeJS configuration gebruiken: TINode-devops'
                sh 'node --version'
                sh 'npm --version'
            }
        }
        stage('Install Dependencies'){
            steps{
                sh 'npm install'
            }
        }
        stage('unittest') {
            steps {
                sh 'npm test'
                junit 'junit.xml'
            }
        }
        stage('Create Bundle') {
            steps {
                sh '''
                mkdir bundle
                cp -r app.js server.js routes.js public package.json package-lock.json bundle/
                zip -r bundle.zip bundle
                '''
                archiveArtifacts artifacts: 'bundle.zip', fingerprint: true
            }
        }

    }
    post {
        success {
            archiveArtifacts artifacts: 'bundle.zip', fingerprint: true
        }
        failure {
            script {
                def date = new Date().format("dd-MM-yyyy HH:mm:ss")
                def errorMessage = "pipeline poging faalt op ${date}\n"
                writeFile file: '/var/lib/jenkins/jenkinserrorlog', text: errorMessage
                echo "Error log written to /var/lib/jenkins/jenkinserrorlog"
            }
        }
    }
}