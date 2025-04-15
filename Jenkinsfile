pipeline {
    agent any
    tools {
        maven 'Maven 3.9.9'  // Ensure this is set in Jenkins Global Tools config
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
         stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
