[200~node('built-in') {
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
    stage('continous testing')
        {
      git branch: 'main', url: 'https://github.com/kailastambe/Functional-testing.git'
      sh 'java -jar /home/ubuntu/.jenkins/workspace/scripted-pipeline/testing.jar'
        }
    stage('continous delivery')
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/scripted-pipeline/webapp/target/webapp.war ubuntu@172.31.37.235:/var/lib/tomcat9/webapps/prodapp.war'
    }
	}
