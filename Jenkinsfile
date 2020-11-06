node
{
  	stage('scm')
  	 { 
    	    git clone 'https://github.com/spring-projects/spring-petclinic.git'
         }
  	stage('build the package')
        {
            sh label: '', script: 'mvn package' 
        }
  	stage('archiving artifacts')
        {
            archive './target/*.jar'
        }
       stage('test results')
       {
           junit './target/surefire-reports'
       }  
}
