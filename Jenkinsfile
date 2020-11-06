


node
{
  stage('scm')
   {
     git 'https://github.com/spring-projects/spring-petclinic.git'
    }
  stage('packaging')
  {
    sh 'mvn package'
   }
  stage('archiving artifacts')
  {
    archive 'target/*.jar'
  }
  stage('junit testing')
   {
     junit './target/surefire-reports'
   }  

}