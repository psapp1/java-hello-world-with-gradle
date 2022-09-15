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
                  echo "JAVA_HOME :::   $JAVA_HOME"
                  sh 'which java'
                  sh 'gradle clean'
             }              
         }
     }
 }
