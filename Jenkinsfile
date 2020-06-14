node {

    stage('git checkout') {

        git branch:'master', url:'https://github.com/rupa-y/repo1.git'

    }

    stage('execute script'){

        sh 'chmod +x script.sh'

        sh 'sh script.sh'

    }

    stage('Email Notification'){
	mail bcc: '', 
	body: """Hi Team,
	Your build number ${env.BUILD_NUMBER} successfully completed. 
	Your job URL is ${env.JOB_URL}
	Your job name is ${env.JOB_NAME}
	
	Git commit id for this change : ${env.GIT_COMMIT}
	Git branch : ${env.GIT_BRANCH}
	This job ran on node : ${NODE_NAME}

Thanks,
DevOps Team""", 
		cc: 'sba@gmail.com', from: '', replyTo: 'sa.b@hotmail.com', subject: "${env.JOB_NAME} Success", 
		to: 'swarupa.yesireddy@gmail.com'
   
   }

}
