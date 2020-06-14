node {

    stage('git checkout') {

        git branch:'master', url:'https://github.com/rupa-y/repo1.git'

    }

    stage('execute script'){

        sh 'chmod +x script.sh'

        sh 'sh script.sh'

    }

    stage('notify by email'){

    emailext body: 'build pass', subject: 'build is good', to: 'swarupa.yesireddy@gmail.com'

    }   

}
