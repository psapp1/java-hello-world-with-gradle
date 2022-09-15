pipeline {
     agent any
     tools {
        gradle "gradle"
    }
     stages {
         stage('Clean Workspace') {
             steps {
                  deleteDir()                  
             }
         }
         stage('Clone Project') {
             steps {                  
                  checkout scm                  
             }
         }
         stage('Build') {
             steps {    
                  sh 'gradle wrapper --gradle-version=5.1.1'
                  sh './gradlew clean build'
             }              
         }
     }
 }
