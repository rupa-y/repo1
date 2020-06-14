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
		You build successfully deployed
		
		Job URL : ${env.JOB_URL}
		Job Name: ${env.JOB_NAME}

                Thanks,
                DevOps Team""", 
		cc: 'sbapatla@gmail.com', from: '', replyTo: 'satya.b@hotmail.com', subject: "${env.JOB_NAME} Success", 
		to: 'swarupa.yesireddy@gmail.com'
   
   }

}
