//declarative script
pipeline{
	agent any
	stages{
		stage("build"){
			steps{
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
	
		
		
		


