pipeline{
	agent any
        tools{
		maven 'Maven'
	}
     stages{	 
     	stage("Build"){
		steps{
		echo "Building"	
		dir('Beers-of-the-World-master\\beeroftheworld') {
		bat label: '', script: 'mvn clean install'
		}
		}
	}
	    stage("Sonar"){
		steps{
		echo "Sonar"
		dir('Beers-of-the-World-master\\beeroftheworld') {
		bat label: '', script: '''mvn sonar:sonar \\
        -Dsonar.projectKey=beeroftheworld:beeroftheworld \\
        -Dsonar.host.url=http://localhost:9000 \\
        -Dsonar.login=tiktok'''
		}
		}
	}
   }
   }

