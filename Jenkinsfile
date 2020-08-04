pipeline{
	agent any
        tools{
		maven 'Maven'
	}
     stages{
     	stage("Build"){
		steps{
		echo "Building"
		bat label: '', script: 'cd Beers-of-the-World-master\\beeroftheworld'
		bat label: '', script: 'mvn clean install'
		}
	}
	    stage("Sonar"){
		steps{
		echo "Sonar"
		bat label: '', script: '''mvn sonar:sonar \\
        -Dsonar.projectKey=pms_backend \\
        -Dsonar.host.url=http://localhost:9000 \\
        -Dsonar.login=tiktok'''
		}
	}
   }
}
