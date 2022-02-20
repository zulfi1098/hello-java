
 node {
	stage('Build') {
		echo "Build"
		sh "ls -la ${pwd()}"
		sh "mkdir -p output"
		writeFile file: "output/somefile", text: "hello world"
		stash name: "firstStash", includes: "output/*"
	}
	stage('Test') {
		echo "Test"
		sleep 30  
		sh "ls -la ${pwd()}/output"
		sh "ls -la ${pwd()}"
	}
	stage('Deploy') {
		echo "Deploy"
	}
	stage('PostDeploy') {
		echo "PostDeploy"
	}
	stage('CleanUpResource') {
		echo "CleanUpResource"
	}
	stage('Ping') {
		echo "Deploy"
		echo "ping google.com"
	}
}



 node  {
 stages {
	 stage('Production') {
			echo "Production"
			dir('firstStash'){
				unstash "firstStash"
			}
			sh "ls -la ${pwd()}"
		}
		 stage('Production2') {
			echo "Production2"
			
		}
 
 }
	

}