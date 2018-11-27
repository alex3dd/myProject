pipeline{
  agent { label 'beanstalk'}
  stages{
    stage('Hello From Github'){
	   steps{
	       echo "Print a message after the build."
		   script{ for (int i=0; i<5;++i) { echo "Hello World ${i}" } }
	   }
	}
  }
}