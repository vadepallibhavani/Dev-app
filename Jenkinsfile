node {
    stage('SCM Checkout') {
        git 'https://github.com/srinivas0256/devapp.git'
    }
    
    stage('Compile-Package') {
        // Get maven home path
        def mvnHome=tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package" 
    }
    stage('Email-Notification') {
        mail bcc: '', body: '''Hi Welcome to Email alerts
Thanks
Srinu''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'sriiniv703@gmail.com'
    }
}