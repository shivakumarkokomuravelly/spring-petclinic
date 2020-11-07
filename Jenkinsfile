




node
{
  stage('scm')
   {
    git 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git'
    }
  stage('packaging')
   {
     sh 'mvn package'
   }
  stage('archive artifacts')
   {
     archive 'target/*.jar'
   }
}



