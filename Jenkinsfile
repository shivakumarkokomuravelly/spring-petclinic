pipeline{
            agent any
            triggers { pollSCM('*/2 * * * *') }
            stages{
                stage('downloading source code'){
                    steps{
                        git branch: 'main', url: 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git'
                    }
                }
                stage('Building the artifacts'){
                    steps{
                        sh 'mvn package'
                    }
                }
                stage('archiving and downloading artifcats'){
                    steps{
                        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
                    }
                }
                stage('displaying junit test results'){
                    steps{
                        junit stdioRetention: '', testResults: 'target/surefire-reports/*.xml'
                    }
                }
            }
          } 
