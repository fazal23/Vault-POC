pipeline {
    agent none 
    stages {
        stage('Set up') {
            agent { dockerfile true } 
            steps {
               
                sh 'echo $HOME'
                
            }
        }
    }
}
