//declarative script
pipeline{
	agent {openjdk:8-jdk-alpine}
	stages{
		stage("build"){
			steps{
				// sh 'maven --version'
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
	
		
		
		


