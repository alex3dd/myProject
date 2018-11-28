pipeline{
  agent { label 'beanstalk'}
  tools{
    maven 'M2'
  }
  
  stages{
    stage('Checkout'){
	   steps{ git "https://github.com/alex3dd/myProject" }
	}
	stage('Build'){
	   steps{ sh 'mvn clear compile' }
	}
	stage('Test'){
	   steps {
	      sh 'mvn test '
		  junit '**/target/surefire-reports/TEST-*.xml'
	   }
	}
	stage('Package'){ steps{ sh 'mvn package' } }
  }
}
