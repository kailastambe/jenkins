node('built-in') {
    stage('continous download') 
    {
    git branch: 'main', url: 'https://github.com/kailastambe/jenkins.git'
    }
    stage('continous build') 
    {
    sh 'mvn package'
    }
   
	}
