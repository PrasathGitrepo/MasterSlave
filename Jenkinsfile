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
					parallel{
					stage('unit test'){ 
						steps{ echo "Running unit Test"}
				}
				stage('Integration Test'){
					agent{
						docker{
							reuseNode false
							image 'ubuntu'
							}
						}
					steps{
						echo "Running Integration Test"	
					     }
						}
			}
	
		}
		
		}
		}
		
		
