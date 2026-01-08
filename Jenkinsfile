pipeline{
            agent any 
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
                stage("Archiving artifacts"){
                    steps{
                        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
                    }
                }
                stage("JUnit Test results"){
                    steps{
                        junit 'target/surefire-reports/*.xml'
                    }
                }
            }
          }
