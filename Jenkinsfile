pipeline {
    agent { dockerfile true } 
    stages {
        stage ('Test 3: Master') {
    when { branch 'master' }
    steps { 
        echo 'I only execute on the master branch.' 
        echo 'Pulling...' + env.BRANCH_NAME
        sh 'python -V'


}

stage ('Test 3: Dev') {
    when { not { branch 'master' } }
    steps {
        echo 'I execute on non-master branches.'
        echo 'Pulling...' + env.BRANCH_NAME
        sh 'python -V'
        sh 'set brf = ${env.BRANCH_NAME} && python abcd.py $brf'
    }
}
        }
}

