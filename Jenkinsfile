pipeline {
    agent any

    tools {
        maven 'maven3.8.6'
    }


    stages {
        stage ('Maven Build') {
            steps {
                script {
                    echo "Building package"
                    sh 'mvn clean package -Dskiptests=true'
                    echo "Checking java version"
                    sh 'java --version'
                    echo ".........."
                
                    
                }
            }
        }
    }


}