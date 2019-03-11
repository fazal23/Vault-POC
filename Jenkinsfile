pipeline {
    agent { dockerfile true} 
    stages {
        stage ('Master') {
    when { branch 'master' }
    steps { 
        echo 'I only execute on the master branch.'
        sh "echo ${env.BRANCH_NAME}"
        sh "python abcd.py ${env.BRANCH_NAME}"
    }
}

stage ('Dev') {
    when { not { branch 'master' } }
    steps {
        sh("printenv")
        echo 'I execute on non-master branches.'
        sh "python abcd.py ${env.CHANGE_BRANCH}"
    }
}
        }
}
