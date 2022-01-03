node('built-in') {
    stage('continous download') 
    {
    git branch: 'main', url: 'https://github.com/kailastambe/jenkins.git'
    }
    stage('continous build') 
    {
    sh 'mvn package'
    }
    stage('continous deployment')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/scripted-pipeline/webapp/target/webapp.war ubuntu@172.31.36.151:/var/lib/tomcat9/webapps/testapp.war'
    }
    
	}
