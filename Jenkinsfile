pipeline{
	agent any
        tool name: 'Maven', type: 'maven'
     stages{
     	stage("Build"){
		steps{
		echo "Building"
		bat label: '', script: 'cd Beers-of-the-World-master\\beeroftheworld'
		bat label: '', script: 'mvn --version'
		}
	}
   }
}
