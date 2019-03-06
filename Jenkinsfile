pipeline {
    agent none 
    stages {
        stage('Set up') {
            agent { dockerfile true } 
            steps {
                withCredentials([usernamePassword(credentialsId: 'vault-root-token', passwordVariable: 'RTOKEN', usernameVariable: 'username'),usernamePassword(credentialsId: 'patoken', passwordVariable: 'PTOKEN', usernameVariable: 'username')]){
                sh 'python /root/abcd.py $PTOKEN $RTOKEN'
               }
             
            }
        }
    }
}
