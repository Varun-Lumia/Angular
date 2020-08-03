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
		bat label: '', script: 'mvn --version'
		}
	}
   }
}
