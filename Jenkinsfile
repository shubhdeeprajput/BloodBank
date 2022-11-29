pipeline{
    agent none
    
    stages{
       
        stage('Pull Repo'){
            steps{
                git 'https://github.com/imShakil/BloodBank.git'
            }
        }
        
        stage('Scan') {
            agent {
                docker { image 'shiftleft/sast-scan' }
            }
            steps {
                sh 'scan --build'
            }
        }
        
    }
    
}
