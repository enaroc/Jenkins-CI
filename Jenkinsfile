pipeline {
    agent any

    tools {
        maven 'maven3.8.6'
    }


    stages {
        stage ('Maven Build') {
            steps {
                script {
                    echo "Testing Code"
                    sh 'mvn clean package -Dskiptests=true'
                    sh 'java --version'
                
                    
                }
            }
        }
    }


}