pipeline {
    agent any 
    stages {        
	stage('Deploy helm') {
	 agent {
           kubernetes {
                 containerTemplate {
                   name 'helm'
                   image 'lachlanevenson/k8s-helm:v3.1.1'
                   ttyEnabled true
                   command 'cat'
              }
            }
         }
         steps {
		container('helm')  { 
	                sh 'helm upgrade -i consumer ./consumer'
		}
            }
        }
    }	     
}
