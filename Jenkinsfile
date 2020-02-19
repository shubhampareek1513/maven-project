pipeline
 {
   agent any

   stages
   
   {
      stage('scm checkout')
       {
         steps
	     {
	    
		 git branch: 'master', url: 'https://github.com/shubhampareek1513/maven-project.git'
	 
	     }
       }
    stage ('validate code')
{
 steps {
withMaven(jdk: 'localjdk', maven: 'local-mvn') {
    sh 'mvn validate'
}
}
}

stage ('test code')
{
 steps {
 
withMaven(jdk: 'localjdk', maven: 'local-mvn') {
    sh 'mvn test'
}
}
}
 }
 }
