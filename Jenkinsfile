pipeline {
    agent any
    tools {
        maven 'apache-maven-3.6.3'
        jdk 'jdk-11.0.5'
        }
        stages {
          
          
             stage('Build') {
                 steps {
                 bat 'mvn install'
                 }
                 post {
                     success {
                         junit 'target/surefire-reports/**/*.xml'
                     }
                  }
                }
           }
      }
