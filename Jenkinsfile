pipeline {

    agent any

    tools {
        // Install the Maven version configured as "M398" and add it to the path.
        jdk 'JDK21'
        maven "M398"
    }

    stages {

        stage('Echo Version') {
            steps {
                echo 'Print Maven Version'
                sh 'mvn -version'
            }
        }

        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                // git branch: 'main', url: 'https://github.com/prasad-rajen/jenkins-hello-world123.git'

                // Run Maven Package CMD
                sh "mvn clean package -DskipTests=true"
            }
        }

        stage('Unit Test') {
            steps {
                sh "mvn test"
            }
        }
    }
}