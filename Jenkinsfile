pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             steps {
                withAWS(region:'us-east-1',credentials:'jenkins') {
                 sh 'echo "Uploading content with AWS credentials"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jen-buck')
                     echo "Multiline shell steps work too"
		     ls -lah
                 '''
              }
         }
     }
}
