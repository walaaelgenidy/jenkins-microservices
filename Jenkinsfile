//declarative script
pipeline{
	 agent any
	 environment {
		 dockerHome = tool 'myDocker'
		 mavenHome = tool 'myMaven'
		 PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	 }
	stages{
		stage("checkout"){
			steps{
				 sh 'mvn --version'
				 sh 'docker version'
				echo "$PATH"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "build"
			}
     	}
		 stage("test"){
			 steps{
                sh "mvn test"
			 }
		 }
		 stage("compile"){
			 steps{
				 sh "mvn clean compile"
			 }
		 }
		 stage("integration test"){
			 steps{
               sh "mvn failsafe:integration-test"
			 }
		 }
	
} 
 post{
	 always{
		 echo "====++++always++++===="
	 }
	 success{
		 echo "====++++only when successful++++===="
	 }
	 failure{
		 echo "====++++only when failed++++===="
	 }
 }
}
	
		
		
		


