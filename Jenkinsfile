pipeline {
  agent any
  options{
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '5')
    disableConcurrentBuilds()
	}
  stages {
    stage('Hello') {
      steps {
        echo "Hola Mundo"
      }
    }
    stage('cat README'){
      when{
        branch "fix-*"
		  }
      step{
        sh '''
          cat README.md
        '''
      }
    }
  }
}

