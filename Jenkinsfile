pipeline {
    agent any 
    stages { 
        stage('Helm upgrade') {
            steps {  
                sh 'helm upgrade -i consumer ./consumer/'
            }
        }
    }	     
}
