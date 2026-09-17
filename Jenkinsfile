pipeline{
    agent any
    stages{
        stage('Checkout') {
            steps{
                git branch: 'main', url: 'https://github.com/Thirisha0306/project.git'
            }
        }
        stage('GenerateReport') {
            steps{
                bat 'python app.py'
            }
        }
        stage('Archive Report'){
            steps{
                archiveArtifacts artifacts: 'report.txt',fingerprint:true
            }
        }
    }
}