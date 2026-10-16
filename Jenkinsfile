pipeline {
	agent any
	stages {
		stage('Build'){
			steps {
				checkout scm
				sh 'echo 123 > test.html'
				stash includes: 'test.html',name: 'app'		
			}
		}
		stage('Test'){ 
                	steps { 
				checkout scm
				unstash 'test.html'
                 		sh 'test -f test.html'
                	}
        	}
	}


}
