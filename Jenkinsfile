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
Your build successfully deployed
	
Job URL : ${env.JOB_URL}
Job Name: ${env.JOB_NAME}

Thanks,
DevOps Team""", 
		cc: 'sba@gmail.com', from: '', replyTo: 'sa.b@hotmail.com', subject: "${env.JOB_NAME} Success", 
		to: 'swarupa.yesireddy@gmail.com'
   
   }

}
