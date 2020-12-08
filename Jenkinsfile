//declarative script
pipeline{
	// agent { docker { image 'maven:3.6.3-openjdk-16' } }
	stages{
		stage("build"){
			steps{
				//  sh 'mvn --version'
				echo "$PATH"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "build"
			}
     	}
		 stage("test"){
			 steps{
                echo "Test"
			 }
		 }
		 stage("integration test"){
			 steps{
               echo " Integration Test"
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
	
		
		
		


