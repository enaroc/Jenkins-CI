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
        stage ('Code Quality Analysis'){
            steps {
                script {
                    echo "Permorming Code Quality Analysis"
                    sh "mvn sonar:sonar"
                }
            }
        }

        stage ('Upload to artifact'){
            steps {
                script {
                    echo "Uploading to Nexus"
                    sh "mvn deploy -Dskiptests=true"
                }
            }
        }
    }


}