pipeline{ 
	agent any
	stages {
	
			stage('One'){ 
				steps{
				   echo "Running Declarative pipeline"
					}
			     }	
			
			stage('two'){ 
				steps{
				   input('Do you want to proceed')
				}
			}
		
		
			stage('three'){ 
				when{
			   		not{ branch "main" }
				}
			   steps{ echo 'hello'
				}
			}
			stage('four'){ 					
					steps{
						echo "Running Integration Test"	
					     }
		
					}
	
		}
		
		}
		
		
		
