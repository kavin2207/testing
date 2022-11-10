node{
	stage('Git Hub'){
		git credentialsId: 'github', url: 'https://github.com/kavin2207/testing'	
	}
	stage('docker image'){
		//bat 'docker buildx create --name mybuilder'
		//bat 'docker buildx use mybuilder'
		
	}
	stage('push to docker hub'){

		withCredentials([usernameColonPassword(credentialsId: 'docker', variable: 'docker')]) {
		    // some block
			bat "docker login -u abhbhatn -p Abhijeet@2209"
		}
		bat 'docker buildx build --platform linux/amd64,linux/arm64,linux/arm/v7 -t abhbhatn/test6:1 --push .'
	}
}
