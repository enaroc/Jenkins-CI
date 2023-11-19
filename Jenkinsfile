pipeline {
    agent any

    tools {
        maven 'maven3.8.6'
    }


    stages {
        stage ('Maven Test') {
            steps {
                script {
                    echo "Testing Code"
                    sh 'mvn test'
                    
                }
            }
        }
    }


}