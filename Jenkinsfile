pipeline {
     agent any
     stages {
         stage('Build') {
             steps {
                 sh 'echo "Hello World and U crazy little programmer"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
             }
         }
         stage('Lint HTML') {
              steps {
                  sh 'tidy -q -e *.html'
              }
         }  
         stage('Deployment message') {
             when {
                branch 'deployment'
            }
              steps {
                  sh 'echo "Deployment branch"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
              }
         }
         stage('Staging message') {
             when {
                branch 'staging'
            }
              steps {
                  sh 'echo "Staging branch"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
              }
         }
         stage('Development message') {
             when {
                branch 'development'
            }
              steps {
                  sh 'echo "Development branch"'
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
              }
         }
     }
}
