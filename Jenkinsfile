

1)jenkins free style(GUI)
2)jenkins CLI
3)scripted pipeline
  groovy
4)declative pipeline




  node
   { 
     stage('scm'){
      
         git 'https://github.com/spring-projects/spring-petclinic.git'
      }
     stage('packaging'){
      
         sh label: '', script: 'mvn package'
      }
     stage('archiving artifacts'){
       
           archive './target/*.jar'
       }
    stage('junit results'){
      
        
        junit './target/surefire-reports/*.xml'
      }
 }



