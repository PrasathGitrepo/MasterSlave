pipeline{ 
	agent any {
		stages{
	
			stage('one'){ steps{
				   echo Running Declarative pipeline
					}
			     }	
			
			stage('two'){ steps{
				   input('Do you want to proceed')
				}
			}
		
		
			stage('three'){ when{
			   	not{ branch "main" }
				}
			   steps{ echo hello
				}
			}
			stage('four'){ 
				parellel{
				stage('unit test'){ 
					steps{ echo "Running unit Test"}
				}}
			stage('Integration Test'){
			agent{
				docker{
					reuseNode false
					image 'ubuntu'
					}
				}
			steps{
				echo 'Running Integration Test'	
			     }
			}
			
	
		}
}}



