pipeline{
            agent any 
              triggers {
        cron('*/1 * * * *')
          }
            stages{
                stage("cloning the code"){
                    steps{
                        git branch: 'main ', url: 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git' 

                    }
                }
                stage("Building the code"){
                    steps{
                        sh 'mvn package'
                    }
                }
                
            }
          }
