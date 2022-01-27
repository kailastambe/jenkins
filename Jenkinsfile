node('built-in') {
    stage('continous download') 
    {
    git branch: 'main', url: 'https://github.com/kailastambe/jenkins.git'
    }
    stage('continous build') 
    {
    sh 'mvn package'
    }
<<<<<<< HEAD
    stage('continous deployment')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/multibranch-pipeline_main/webapp/target/webapp.war ubuntu@172.31.36.151:/var/lib/tomcat9/webapps/testapp.war'
    }
    
=======
   
>>>>>>> fb2e8400dee5974d5d17886300b2038b1ad04d5f
	}
