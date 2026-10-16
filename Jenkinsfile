pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
				checkout scm
				sh 'echo 123 > test.html'		
			}
		}
		stage('Test'){ 
                	steps { 
				checkout scm
                 		sh 'test -f test.html'
                	}
        	}
	}


}
