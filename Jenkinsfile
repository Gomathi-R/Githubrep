node{
   stage('SCM Checkout'){
     git 'https://github.com/Smaheshwar85/easeWithbase'
   }
   stage('Compile-Package'){
      def mvnHome =  tool name: 'Mavan3', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   
     }
    stage('Email Notification'){
     mail bcc: '', body: '''Build successful!!!!

Thanks,
Mahesh''', cc: '', from: '', replyTo: '', subject: 'Build successfull', to: 'smahesh2305@gmail.com'
   }
}
