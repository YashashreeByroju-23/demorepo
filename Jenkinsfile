@Library('my-shared-library') _
pipeline {
    agent any 
    tools {
        maven 'mvn3.9.12'
        java 'java17'
    }
    stages {
        stage ('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/YashashreeByroju-23/simple-java-app.git'
            }
            
        }
        stage('Build') {
            steps {
                mavenBuild()
            }
        }
        stage ('Post-build') {
            steps {
                echo 'Build successful'
            }
        }
    }
}
