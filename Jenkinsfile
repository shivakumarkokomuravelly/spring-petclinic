pipeline {
    agent any 
    triggers { pollSCM('*/2 * * * *') }
    stages {
        stage('Downloading source code ') {
            steps {
                git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'

            }
        }
        stage('creating artifact'){
            steps{
                sh 'mvn package'

            }
        }
        stage('archiving artifacts'){
            steps{
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
            }
        }
        
    }
}     