pipeline {
    agent any
    
    stages {
	   
	    
            stage('Compile and Clean') { 
                steps {
                      bat 'mvn clean install'
                      }
            }
       
	        stage('Junit5 Test') { 
                 steps {
	               //bat 'mvn test'
			 echo 'test'
                  }
            }

	    stage('Jacoco Coverage Report') {
        	     steps{
            		//jacoco()
            		echo 'TestCoverage'
		          }
	        }
		stage('SonarQube'){
			steps{
			//	bat label: '', script: '''mvn sonar:sonar \
			//	-Dsonar.host.url=http://CDLVDIDEVMAN500:9000 \
			//	-Dsonar.login=c0909bf6713cd534393d47364d1da553431a220d'''
			echo 'Sonar Code Scanning '
				}	
   			}
        stage('Maven Build') { 
            steps {
                bat 'mvn clean install'
                  }
            }
        stage('Build Docker image'){
           steps {
                      //   	docker build -t nodejs-server -f Dockerfile.arg --build-arg UBUNTU_VERSION=18.04
		             //--build-arg CUDA_VERSION=10.0
                     //bat 'docker build -t  docker.repository.esi.adp.com/clientcentral/training:docker_jenkins_springboot:${BUILD_NUMBER} .'
           	  //  bat 'docker build -t  jenkinssampleproject --build-arg VER=1.0 .'
           	  echo 'integration'
		         }
             }
        stage('Docker Login'){
            steps {
              echo "docker login from console"
                //docker login docker.repository.esi.adp.com -u clientcentralcicd -p $adpdtrrepopassword
            }                
        }
        stage('Docker Push'){
            steps {
				  echo "docker login from console"
              //  bat 'docker push aruna708/jenkinssampleproject'
            }
        }
        stage('Docker deploy'){
            steps {
				  echo "docker login from console"
               // bat 'docker run -itd -p  8086:8086 jenkinssampleproject'
             }
        }
    
     
    }
}
