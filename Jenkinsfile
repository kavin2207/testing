node{
	stage('Git Hub'){
		git credentialsId: 'github', url: 'https://github.com/kavin2207/testing'	
	}
	stage('docker image'){
		bat 'docker buildx build --platform linux/amd64,linux/arm64,linux/arm/v7 -t abhbhatn/test5:1 .'
	}
	stage('push to docker hub'){

		withCredentials([usernameColonPassword(credentialsId: 'docker', variable: 'docker')]) {
		    // some block
			bat "docker login -u abhbhatn -p Abhijeet@2209"
		}
		bat "docker push abhbhatn/test5:1"
	}
}
