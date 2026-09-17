pipeline{
    agentany
    stages{
        stage('Checkout') {
            steps{
                git branch: 'main', url: 'https://github.com/Thirisha0306/project.git'
            }
        }
        stage('GenerateReport') {
            steps{
                bat 'pythonapp.py'
            }
        }
        stage('ArchiveReport'){
            steps{
                archiveArtifacts artifacts: 'report.txt',fingerprint:true
            }
        }
    }
}