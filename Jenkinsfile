pipeline{
    agent any
    stages{
        stage('Git checkout'){
            steps{
               git credentialsId: 'github', url: 'https://github.com/Ram9500/sample.git'
            }
        }
    }
}

