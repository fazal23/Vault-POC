pipeline {
    agent { dockerfile true} 
    stages {
        stage ('Master') {
    when { branch 'master' }
    steps { 
        echo 'I only execute on the master branch.'
        sh "echo ${env.BRANCH_NAME}"
    }
}

stage ('Dev') {
    when { not { branch 'master' } }
    steps {
        echo 'I execute on non-master branches.'
        sh "echo ${env.BRANCH_NAME}"
    }
}
        }
}
