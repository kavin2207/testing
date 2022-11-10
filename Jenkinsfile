node{
	stage('Git Hub'){
		git credentialsId: 'github', url: 'https://github.com/kavin2207/testing'	
	}
	stage('docker image'){
		bat 'docker build -t abhbhatn/test3:1 .'
	}
	stage('push to docker hub'){

		withCredentials([usernameColonPassword(credentialsId: 'docker', variable: 'docker')]) {
		    // some block
			bat "docker login -u abhbhatn -p Abhijeet@2209"
		}
		bat "docker push abhbhatn/test3:1"
	}
}
