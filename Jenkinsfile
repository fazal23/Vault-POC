pipeline {
    agent { dockerfile true} 
    stages {
        stage ('Master') {
    when { branch 'master' }
    steps { 
        echo 'I only execute on the master branch.'
        echo 'Pulling...' + env.BRANCH_NAME
        sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
    }
}

stage ('Dev') {
    when { not { branch 'master' } }
    steps {
        echo 'I execute on non-master branches.'
        echo 'Pulling...' + env.BRANCH_NAME
        sh "echo ${env.WORKSPACE}"
    }
}
        }
}
