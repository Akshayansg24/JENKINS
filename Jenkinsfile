pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                  git url: 'https://github.com/Akshayansg24/JENKINS.git', credentialsId: 'github token' 
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build React App') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Deploy Locally') {
            steps {
                bat 'deploy.bat'
            }
        }
    }
}
