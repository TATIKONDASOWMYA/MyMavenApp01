pipeline{
	agent any
	
	tools{
	maven 'Maven'
	}
	
	stages{
		stage('Checkout'){
		steps{
		git branch: 'master' , url:'https://github.com/TATIKONDASOWMYA/MyMavenApp01.git'
		}
		}
		stage('Build'){
		steps{
		sh 'mvn clean package'
		}
		}
		stage('Test'){
		steps{
		sh 'mvn test'
		}
		}
		stage('Run'){
		steps{
		sh 'java -jar target/MyMavenApp01-1.0-SNAPSHOT.jar'
		}
		}
	}
	post{
		success{
			echo 'Build Success'
			}
		failure{
			echo 'Build Failure'
			}
	}
}


		
