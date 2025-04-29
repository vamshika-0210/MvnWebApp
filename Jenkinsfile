pipeline {
    agent any

    tools {
        maven 'Maven_3.8.7'
        jdk 'JDK_17'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/vamshika-0210/MvnWebApp.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy WAR') {
            steps {
                // Replace with your actual remote details
                sh 'scp target/MymavenWebApp01.war user@your-server:/path/to/tomcat/webapps/'
            }
        }
    }
}
