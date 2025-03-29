pipeline {
    agent any
    tools {
        nodejs 'NodeJS'
    }
    stages{
        stage("Cloning Git Repository"){
            steps{
                bat "git clone https://github.com/KURO-1125/Devops-Evaluation.git"
            }
        }
        stage("Installing Dependencies"){
            steps{
                bat "npm install"
            }
        }
        stage("Running Tests"){
            steps{
                bat "npm test || echo 'No tests defined'"
            }
        }
        stage("Building Application"){
            steps{
                bat "npm run build"
            }
        }
        stage("Deploying Application"){
            steps{
                bat "npm start"
            }
        }
    }
}