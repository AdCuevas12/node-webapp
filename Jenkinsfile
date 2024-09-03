
pipeline {
   agent { label 'linux-node' }
   stages {
       stage('Build') {
           steps {
               script {
                   sh 'docker build -t node-app .'
               }
           }
       }
       stage('Deploy') {
           steps {
               script {
                    sh 'docker run -d -p 3000:3000 node-app'
               }
           }
       }
   }
}
