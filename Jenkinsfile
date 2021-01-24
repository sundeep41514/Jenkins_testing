pipeline { 
    agent any
    stages {
      stage('step 1'){
		  steps{
		       //echo "sundeep"
		       //sh 'python prc.py'
		      //sh 'python */demo.py'
				echo 'Hi, starting the pipeline'
           }
        }
		stage('step 2'){
			steps{
				echo input('Do you want to proceed')
			}
		}
		stage('step 3'){
			when{
				not{
					branch 'master'
				}
			}
			steps{
				echo 'Hello there'
			}
		}
		stage('stage 4')
		{
			parallel{
				stage('unit test'){
					steps{
						echo 'Running the unit test'
					}
				}
				stage('Integration test'){
					steps{
						echo 'Running the integration test..'
					}
				}
			}
		}
    }
}