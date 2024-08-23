pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                mvn -B -DskipTests clean package
            }
        }
    }
}