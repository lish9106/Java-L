pipeline {
    agent { label 'J-slave-1' }
    stages {
        stage ('Compile Stage'){
            steps{
                withMaven(maven:'maven3.8.2'){
                sh 'mvn clean compile'
                }
            }
        }

        stage ('Test Stage'){
            steps{
                withMaven(maven:'maven3.8.2'){
                sh 'mvn test'
                }
            }    
        }

        stage ('Deploy Stage'){
            steps{
                withMaven(maven:'maven3.8.2'){
                sh 'mvn deploy'
                }
            }    
        }
    }   
}
