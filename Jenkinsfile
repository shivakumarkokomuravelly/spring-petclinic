pipeline {
    agent any 
    
    stages {
        stage('git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/shivakumarkokomuravelly/spring-petclinic.git'
            }
        }
        stage('Build artifcat'){
            steps{
                sh 'mvn package'

            }
        }
        stage('Archiving artifacts'){
            steps{
                archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false

            }
        }
        stage('publishing junit test results'){
            steps{
                junit 'target/surefire-reports/*.xml'

            }
        }
    }
}
