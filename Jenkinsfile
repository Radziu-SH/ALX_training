pipeline {
	agent any
	options{
		timestap()
	}
		stages {
			stage('Build'){
				steps {
					checkout scm
					sh 'echo 123 > test.html'
					stash includes: 'test.html', name: 'html'
					archiveArtifacts artifacts: 'test.html', fingerprint: true		
				}
			}
			stage('Test'){ 
                		steps { 
					checkout scm
					unstash 'html'
                 			sh 'test -f test.html'
                			}
        			      }
			}

	


}
