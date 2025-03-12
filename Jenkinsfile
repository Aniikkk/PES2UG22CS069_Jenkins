pipeline {
     agent any
 
     stages {
         stage('Build') {
             steps {
                 script {
                    //Intentional error: non-existing file
                     sh 'g++ -o PES2UG22CS069-1 meh.cpp'
                 }
             }
         }
         stage('Test') {
             steps {
                 script {
                     sh './PES2UG22CS069-1'
                 }
             }
         }
         stage('Deploy') {
             steps {
                 echo 'Deploying the application...'
             }
         }
     }
 
     post {
         failure {
             echo 'Pipeline failed'
         }
     }
 }
